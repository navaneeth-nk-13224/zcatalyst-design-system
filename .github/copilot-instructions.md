# ZCatalyst Design System — Copilot MCP Workflow

> **This file is auto-loaded by GitHub Copilot.** It contains the complete workflow for building Figma pages using the ZCatalyst Design System via `figma-console-mcp`.

---

## Prerequisites

- **Figma Console MCP** server running and connected
- **ZCatalyst Design System** file linked (read-only DS file)
- **Working Figma file** with a "Layout Template" page containing a Layout component instance
- Reference docs: `docs/zcatalyst-design-system.md`, `docs/zcatalyst-styles.md`, `docs/rules.md`

---

## Execution Protocol (1–2 calls per page)

1. **Call 1**: Clone+detach layout → import variables → load fonts → build ALL content in one `figma_execute`
2. **Call 2** (optional): Continue building if Call 1 timed out, or audit variable bindings
- NEVER rebuild layout from scratch. NEVER exceed 2 calls per page.

---

## Step 1: Layout Clone + Detach

Always start by cloning the Layout from the Layout Template page:

```js
// 1. Find Layout INSTANCE on Layout Template page
const layoutPage = figma.root.children.find(p => p.name === 'Layout Template');
await figma.setCurrentPageAsync(layoutPage);
const layoutInst = layoutPage.findOne(n => n.name === 'Layout' && n.type === 'INSTANCE');

// 2. Clone to new page
const pg = figma.createPage();
pg.name = 'PAGE_NAME';
const cl = layoutInst.clone();
pg.appendChild(cl);
await figma.setCurrentPageAsync(pg);

// 3. CRITICAL: detach top-level to allow appendChild (inner components stay as INSTANCE)
const det = cl.detachInstance();

// 4. Hide Sub Header, prepare Container
const subH = det.findOne(n => n.name === 'Sub Header' && n.type === 'INSTANCE');
if (subH) subH.visible = false;
const container = det.findOne(n => n.name === 'Container');
container.layoutMode = 'VERTICAL';
container.primaryAxisSizingMode = 'AUTO';
container.layoutSizingHorizontal = 'FILL';
container.itemSpacing = 20;
for (const k of [...container.children]) k.remove();
// BUILD CONTENT INSIDE container
```

**Key facts:**
- `detachInstance()` converts the top-level INSTANCE→FRAME, but all inner components (ServiceMenu, Header, Sidemenu, Sub Header) remain as INSTANCE
- Without detach: `appendChild` throws "Cannot move node into instance"
- Container defaults to HORIZONTAL after clone — always set `layoutMode='VERTICAL'`

---

## Step 2: Batch Variable Import

Paste this at the top of every `figma_execute` call to import all needed design variables:

```js
const V = {};
const VK = {
  txtPrimary:      '923bd06a923fee3c9811bed53c2e1023d667e99f',
  txtSecondary:    'cbc2c154ea80793b1cc0707f853d43e59a96cf04',
  txtLight:        '7a19681638a68e906bddd75586271d7836762473',
  txtWhite:        '3b9a2f87cd7cb2db22e52bba6c1fe2ba97a31b0e',
  txtTheme:        '0e6d1bdb08c318e876eafd4be5915c3266191fae',
  txtDisable:      '34cb78323c4482bb9ddd65aa567b609282734f7b',
  bodyBg:          '8a73e5eb7acb073d9207bddf09a19287115b4cfd',
  containerBg:     'a9b4ed83b5ad5b5fe00bc4e56a141e92ad8dae02',
  borderDefault:   'dee9b282355cc41a5865a29cc8fc48d6b80484ec',
  cardsBgPrimary:  '5f31ffd455f693c79bb692d089dc99c045508bde',
  cardsBorderDefault: '511f1c30128041f0816ec4025aed7cc050584519',
  theme1:          'ce98fc91700925c5828b0649694ce8d694537610',
  iconPrimary:     '5a84f2ed810016b3efb87e427e84cc49562309fa',
  iconSecondary:   '4b949396ae9456a5e3e8c5f211b2904a88ac33c0',
  iconTheme:       'ff104a7fb5d301d5943d7172ed0beef76aa1fece',
  iconLight:       'b477aff637a8016f87deb55b8d1aa6a43b0f5e6e',
  outerDivider:    '71abb67e509670e8bc2a18aecd730ae64a7eb0d7'
};
await Promise.all(Object.entries(VK).map(async ([k, v]) => {
  V[k] = await figma.variables.importVariableByKeyAsync(v);
}));
await Promise.all([
  figma.loadFontAsync({ family: 'Inter', style: 'Regular' }),
  figma.loadFontAsync({ family: 'Inter', style: 'Medium' }),
  figma.loadFontAsync({ family: 'Inter', style: 'Semi Bold' })
]);
```

### Semantic Color Variables (for badges, dots, status indicators)

> **WARNING**: BADGE and TIMELINE variable keys are NOT importable — they throw "could not find variable" errors. Use OTHER SHADES keys instead.

```js
// Add these to VK when you need status colors:
green1: 'c5b468027686a2c9dc6e05aeac52f132148b8770',  // #29B260 — green dots, text
green4: 'f83e5196695146c60ada6141fc9037940c520346',  // #EAF7EF — green light bg
red1:   '7da69489ce9f98f8ddfb85a66724a1d6d74fb409',  // #E22020 — red dots, text
red4:   '5dc42d49093cedf272fbcf74f6da1009406fd2b8',  // #FFEFEF — red light bg
orange1:'d1a680043888628f6988e070a825a235984cc094',  // #C98E06 — orange dots, text
orange4:'196dd6808474b55bb51f7959f6884c003909651c',  // #FFF3D7 — orange light bg
```

---

## Step 3: Helper Functions

Paste these after the variable import block:

```js
function setFill(n, v) {
  n.fills = [figma.variables.setBoundVariableForPaint(
    { type: 'SOLID', color: { r: 0, g: 0, b: 0 } }, 'color', v
  )];
}

function setStroke(n, v) {
  n.strokes = [figma.variables.setBoundVariableForPaint(
    { type: 'SOLID', color: { r: 0, g: 0, b: 0 } }, 'color', v
  )];
}

// Frame builder — used for every section/row/card
function mkF(parent, opts = {}) {
  const f = figma.createFrame();
  f.layoutMode = opts.dir || 'VERTICAL';
  f.primaryAxisSizingMode = opts.hug ? 'HUG' : 'AUTO';
  f.counterAxisSizingMode = 'AUTO';
  f.itemSpacing = opts.gap ?? 8;
  f.paddingTop = f.paddingBottom = f.paddingLeft = f.paddingRight = 0;
  f.fills = []; f.clipsContent = false;
  parent.appendChild(f);
  f.layoutSizingHorizontal = opts.fillW !== false ? 'FILL' : 'HUG';
  if (opts.pad) { f.paddingTop = f.paddingBottom = f.paddingLeft = f.paddingRight = opts.pad; }
  if (opts.padX) { f.paddingLeft = f.paddingRight = opts.padX; }
  if (opts.padY) { f.paddingTop = f.paddingBottom = opts.padY; }
  if (opts.bg) { setFill(f, opts.bg); }
  if (opts.border) { setStroke(f, opts.border); f.strokeWeight = 1; }
  if (opts.radius) { f.cornerRadius = opts.radius; }
  if (opts.align) { f.counterAxisAlignItems = opts.align; }
  return f;
}

// Text builder — applies text style + color variable
async function mkText(parent, text, styleKey, colorVar, opts = {}) {
  const t = figma.createText();
  const s = await figma.importStyleByKeyAsync(styleKey);
  await t.setTextStyleIdAsync(s.id);
  t.characters = text;
  setFill(t, colorVar);
  if (opts.width) { t.resize(opts.width, t.height); t.textAutoResize = 'HEIGHT'; }
  parent.appendChild(t);
  if (opts.fill) t.layoutSizingHorizontal = 'FILL';
  return t;
}

// Component importer
async function addComp(parent, compKey, opts = {}) {
  const c = await figma.importComponentByKeyAsync(compKey);
  const i = c.createInstance();
  parent.appendChild(i);
  if (opts.fill) i.layoutSizingHorizontal = 'FILL';
  return i;
}

// Text overrides on component instances
async function setText(inst, nodeName, txt) {
  const tn = inst.findOne(n => n.type === 'TEXT' && n.name === nodeName);
  if (tn) { await figma.loadFontAsync(tn.fontName); tn.characters = txt; }
}

async function setLongText(inst, txt) {
  const tn = inst.findAll(n => n.type === 'TEXT').find(n => n.characters?.length > 20);
  if (tn) { await figma.loadFontAsync(tn.fontName); tn.characters = txt; }
}
```

---

## Text Style Keys (quick reference)

| Style | Key |
|---|---|
| Headlines/H4 | `5773e80e10f3396d8da80218ae0e7799637c42e3` |
| Headlines/H5 | `be57224f7a8d40f6fb33855456c324c6fdc58adc` |
| Body/Body 1 (14px) | `dd4a720e10df4ebca0fc96607ae81effb512009e` |
| Body/Body 2 (16px) | `3ec92fcb0c18950b4de40b4b0481d6411327af2f` |
| Body/Body 3 (12px) | `540b559794ca7eb23631093b727eddd1d41c14b7` |

Full list: `docs/zcatalyst-styles.md`

---

## Common Component Keys (quick reference)

| Component | Key |
|---|---|
| Fill Button | `30cdc2a5cef8cec1c194d46e4ab7c3670b16703c` |
| Outline Button | `8a0ada51ba975510e367002fad3fdbf6b1770e93` |
| TextBox | `eec333f0fddc7c20cd07b2827a2240784af309ba` |
| Dropdown | `268ef50c7501a029a7b5179168be06dd7ee0fc3e` |
| Divider | `f72c745f6cb854f7aa17f057f65855d67ab9dbaf` |
| Arrow Left | `107e6552f7200e0fe2e80f07109e343ed57c8c51` |
| Copy Icon | `bf61e378330f2257af023cb6db96202828cb98a8` |
| Three Dot Menu | `28ee9e6ed927d74b8a4a08cc0dff4f3439763f73` |

Full list: `docs/zcatalyst-design-system.md`

---

## Building Patterns (proven templates)

### Card with header + content
```js
const card = mkF(container, { pad: 16, bg: V.cardsBgPrimary, border: V.cardsBorderDefault, radius: 8 });
await mkText(card, 'Card Title', 'be57224f7a8d40f6fb33855456c324c6fdc58adc', V.txtPrimary); // H5
const content = mkF(card, { gap: 12 });
// add fields, components, etc. to content
```

### Row of stat cards
```js
const row = mkF(container, { dir: 'HORIZONTAL', gap: 16 });
for (const [label, value] of [['Total', '156'], ['Active', '142']]) {
  const card = mkF(row, { pad: 16, bg: V.cardsBgPrimary, border: V.cardsBorderDefault, radius: 8 });
  await mkText(card, value, '5773e80e10f3396d8da80218ae0e7799637c42e3', V.txtPrimary); // H4
  await mkText(card, label, '540b559794ca7eb23631093b727eddd1d41c14b7', V.txtSecondary); // Body 3
}
```

### Title row (heading + button, no spacer)
```js
const titleRow = mkF(container, { dir: 'HORIZONTAL', gap: 16, align: 'CENTER' });
await mkText(titleRow, 'Page Title', '5773e80e10f3396d8da80218ae0e7799637c42e3', V.txtPrimary, { fill: true }); // FILL pushes button right
const btn = await addComp(titleRow, '8a0ada51ba975510e367002fad3fdbf6b1770e93'); // Outline btn
await setText(btn, 'Button Text', 'Action');
```

### Form section with label + input fields
```js
const section = mkF(container, { pad: 20, bg: V.cardsBgPrimary, border: V.cardsBorderDefault, radius: 8, gap: 16 });
await mkText(section, 'Section Title', 'be57224f7a8d40f6fb33855456c324c6fdc58adc', V.txtPrimary); // H5
await addComp(section, 'f72c745f6cb854f7aa17f057f65855d67ab9dbaf', { fill: true }); // Divider
const fieldRow = mkF(section, { dir: 'HORIZONTAL', gap: 16 });
await addComp(fieldRow, 'eec333f0fddc7c20cd07b2827a2240784af309ba', { fill: true }); // TextBox
await addComp(fieldRow, 'eec333f0fddc7c20cd07b2827a2240784af309ba', { fill: true }); // TextBox
```

### Status badge (green/red/orange)
```js
const badge = mkF(parent, { dir: 'HORIZONTAL', gap: 4, padX: 8, padY: 3, fillW: false, radius: 4, bg: V.green4, align: 'CENTER' });
const dot = figma.createEllipse(); dot.resize(6, 6); setFill(dot, V.green1); badge.appendChild(dot);
await mkText(badge, 'Active', '540b559794ca7eb23631093b727eddd1d41c14b7', V.green1); // Body 3
```

### Progress bar
```js
// Use fixed-width rectangles, NOT layoutGrow (only accepts 0 or 1)
const track = mkF(parent, { dir: 'HORIZONTAL', gap: 0, radius: 4, bg: V.borderDefault });
track.resize(400, 8); track.clipsContent = true;
const fill = figma.createRectangle(); fill.resize(pct * 4, 8); // pct = percentage
setFill(fill, V.theme1); track.appendChild(fill);
```

---

## Component Text Node Names

| Component | Text Node Name |
|---|---|
| Button / GradientButton / Link | `Button Text` |
| TextBox | `Text Field` (label), `Enter Label Text` (placeholder) |
| TextArea | `Text Area` (label), `Enter Label Text` (placeholder) |
| Dropdown | `Drop down` (label), `Select List` (placeholder) |
| Search | `Search Here` |
| Chip | `Active list` |
| Accordion | `Main Text` (heading), `Sub Text` (description) |
| Alerts | heading text, lorem text, `Button Text` (action) |
| AttentionBox | `Attention Heading`, lorem text, `Button Text` |
| Breadcrumbs | `Breadcrumb Link` (6×, each segment) |
| Tabs | `Tab Text 1` – `Tab Text 5` |
| FileUpload | `Upload File` (label), `Select a file or...` |
| Checkbox / Radio / Toggle | title via `Title Text` BOOL prop |

---

## Toggling Component Properties

```js
// Via figma_set_instance_properties MCP tool:
figma_set_instance_properties({ nodeId: 'X:Y', properties: { 'Icon Left': true, 'Show Tab 5': false } })
```

Property names auto-resolve `#nodeId` suffixes — just use the base name.

---

## Layout Structure (inside Layout Template)

```
Layout (1582×860, VERTICAL)
└─ Layout with Side menu (HORIZONTAL, gradient)
   ├─ ServiceMenu (INSTANCE)
   └─ Right Column (VERTICAL, FILL)
      ├─ Header (INSTANCE)
      └─ Below Header (HORIZONTAL, FILL)
         ├─ Sidemenu (INSTANCE)
         └─ Content Column (VERTICAL, FILL)
            ├─ Sub Header (INSTANCE, usually hidden)
            └─ Body (FILL, padding 14, bodyBg)
               └─ Container (FILL, white, corner 8, border 1px, padding 16) ← BUILD HERE
```

---

## MCP Tool Quick Reference

| Tool | Use For |
|---|---|
| `figma_execute` | ALL design building (timeout max 30s) |
| `figma_capture_screenshot` | Verify current state of the page |
| `figma_set_instance_properties` | Toggle BOOL/VARIANT props on instances |
| `figma_search_components` | Find components by name |
| `figma_get_component_details` | Get component metadata |
| `figma_clone_node` | Clone any node by ID |
| `figma_set_text` | Quick text override by nodeId |
| `figma_resize_node` | Resize any node by nodeId |

---

## Gotchas & Lessons Learned

1. **BADGE/TIMELINE variables don't import** — Use OTHER SHADES collection keys (Green 1–4, Red 1–4, Orange 1–4) for semantic colors.
2. **`layoutGrow` only accepts 0 or 1** — For progress bars, use fixed-width rectangles inside a clipped auto-layout track.
3. **`primaryAxisSizingMode` only accepts `'FIXED'` or `'AUTO'`** — No other values are valid.
4. **Timeout recovery** — If `figma_execute` times out (30s), content is partially built. Query what exists, then continue from there — never rebuild from scratch.
5. **Variant switching via `getComponentSetAsync()`** can throw "not a function" — Safer to import a different component type directly.
6. **Alerts text override** — heading text node has no consistent name. Use `findAll(TEXT).find(n => n.characters?.includes('Alert'))`.
7. **AttentionBox body text** — Use `setLongText()` helper to find the first text node with >20 characters.
8. **Import only needed vars** — When continuing a partial build, import only the VK entries you need to save execution time.
9. **Page deletion** — Cannot remove the current page. Switch to another page first, then delete.

---

## Audit (optional verification)

Run this after building to check for unbound color fills:

```js
const issues = [];
det.findAll(n => {
  if ('fills' in n && n.fills?.length) {
    const f = n.fills[0];
    if (f.type === 'SOLID' && !f.boundVariables?.color) issues.push(n.name + ' (' + n.id + ')');
  }
});
return issues.length ? 'Unbound: ' + issues.join(', ') : 'All OK';
```

---

## Mandatory Rules

See `docs/rules.md` for the complete list of 12 mandatory rules that must be followed for every build.
