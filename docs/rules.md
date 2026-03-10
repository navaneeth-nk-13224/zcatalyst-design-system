# ZCatalyst Design System — Design Rules

> **Read this file before creating any Figma page using the MCP workflow.**
> These rules prevent known errors and ensure consistent, high-quality output.

---

## Mandatory Rules

0. **ALL frames = auto layout** — NEVER group elements. Every container must use `layoutMode='VERTICAL'|'HORIZONTAL'` with proper auto layout. Keep layer names clean and descriptive. No manual positioning.

1. **ALL colors = variables** — Never use raw hex values. Always bind colors via `setFill(node, V.variable)` using imported design variables.

2. **ALL UI elements = components** — Every button, input, badge, toggle, etc. MUST be an imported component instance. Never recreate UI elements from scratch.

3. **ALL text = text styles** — Use `await t.setTextStyleIdAsync(s.id)` to apply text styles. Do NOT use the sync setter `t.textStyleId = s.id` — it throws an error with `documentAccess: dynamic-page`.

4. **Styles reference** — Look up text style keys and color variable keys from `docs/zcatalyst-styles.md` before building.

5. **FILL after appendChild** — `layoutSizingHorizontal='FILL'` MUST be set AFTER `parent.appendChild(node)`. Setting it before throws an error.

6. **Cannot appendChild to INSTANCE** — You must call `detachInstance()` first or use plain frames. Direct append to component instances is not allowed.

7. **Async APIs only** — Use `getVariableByIdAsync`, `getMainComponentAsync`, `importComponentByKeyAsync`, etc. Sync versions do not exist in the Plugin API.

8. **Variable paint binding** — Use `setBoundVariableForPaint()` to bind color variables. Do NOT use `setBoundVariable('fills', ...)`.

9. **No opacity in fills** — Fill paint objects ignore opacity. Use `node.opacity` separately.

10. **Never set FILL on component internals** — Only set `layoutSizingHorizontal='FILL'` on direct children you create. Touching internal nodes of component instances breaks icons and layout.

11. **No spacer frames in title rows** — Instead of adding an empty frame as a spacer, set the heading text to `layoutSizingHorizontal='FILL'` so it naturally pushes buttons to the right.

12. **BADGE/TIMELINE variables don't import** — Use OTHER SHADES collection keys (Green 1–4, Red 1–4, Orange 1–4) for semantic colors. BADGE and TIMELINE keys throw "could not find variable" errors.

13. **`layoutGrow` only accepts 0 or 1** — For progress bars, use fixed-width rectangles inside a clipped auto-layout track. Do NOT use fractional values.

14. **`primaryAxisSizingMode` only accepts `'FIXED'` or `'AUTO'`** — No other values are valid.

15. **Timeout recovery** — If `figma_execute` times out (30s), content is partially built. Query what exists, then continue from there — never rebuild from scratch.

16. **Page deletion** — Cannot remove the current page. Switch to another page first, then delete.

17. **DS file is READ-ONLY** — Never add, build, modify, or change anything in the Design System file. It is a published library — only import components and variables from it.

18. **Always use DS components over hand-built elements** — If a component exists in the DS (Badges, Table, Tabs, etc.), import it. Never recreate UI elements with raw frames, ellipses, or text — even to save execution time during timeouts. Split work across multiple calls instead.

---

## Importable Semantic Color Variables

> Only keys from the **OTHER SHADES** collection are importable. BADGE and TIMELINE collection keys will fail.

| Variable | Key | Hex (Light) | Use For |
|---|---|---|---|
| Green 1 | `c5b468027686a2c9dc6e05aeac52f132148b8770` | #29B260 | Green dots, text |
| Green 4 | `f83e5196695146c60ada6141fc9037940c520346` | #EAF7EF | Green light bg |
| Red 1 | `7da69489ce9f98f8ddfb85a66724a1d6d74fb409` | #E22020 | Red dots, text |
| Red 4 | `5dc42d49093cedf272fbcf74f6da1009406fd2b8` | #FFEFEF | Red light bg |
| Orange 1 | `d1a680043888628f6988e070a825a235984cc094` | #C98E06 | Orange dots, text |
| Orange 4 | `196dd6808474b55bb51f7959f6884c003909651c` | #FFF3D7 | Orange light bg |

---

## Helper Functions

These must be pasted into every `figma_execute` call after the variable import block:

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

async function addComp(parent, compKey, opts = {}) {
  const c = await figma.importComponentByKeyAsync(compKey);
  const i = c.createInstance();
  parent.appendChild(i);
  if (opts.fill) i.layoutSizingHorizontal = 'FILL';
  return i;
}

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

## Building Patterns

### Card with header + content
```js
const card = mkF(container, { pad: 16, bg: V.cardsBgPrimary, border: V.cardsBorderDefault, radius: 8 });
await mkText(card, 'Card Title', 'be57224f7a8d40f6fb33855456c324c6fdc58adc', V.txtPrimary); // H5
const content = mkF(card, { gap: 12 });
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
await mkText(titleRow, 'Page Title', '5773e80e10f3396d8da80218ae0e7799637c42e3', V.txtPrimary, { fill: true });
const btn = await addComp(titleRow, '8a0ada51ba975510e367002fad3fdbf6b1770e93'); // Outline btn
await setText(btn, 'Button Text', 'Action');
```

### Status badge (use Badges component — NEVER hand-build)
```js
// Green badge
const badge = await addComp(parent, '8ca7161ecb86188fe2ab3881babe81a04c22c56c'); // Badges: Primary, Green, Default
await setText(badge, '1', 'Active');
// Red badge
const redBadge = await addComp(parent, 'e25c954ef6fdb7830d089cb529d3122e554fbd7b'); // Badges: Primary, Red, Default
await setText(redBadge, '1', 'Failed');
// Orange badge
const orangeBadge = await addComp(parent, '67c996cc2e2e5af5cd59e9a4ea521693096370bc'); // Badges: Primary, Orange, Default
await setText(orangeBadge, '1', 'Pending');
```

#### Badge variant keys
| Color | Default | Small | Dot |
|---|---|---|---|
| Primary | `5d541380661e1a2de2cfb5557b50b58d8ff53425` | `7e9959c67a04d3bc86d044d6c7ff0ec5c0c40e46` | `32eb7f5e36be45eafc9b50ca25c371bbf1c4b17e` |
| Green | `8ca7161ecb86188fe2ab3881babe81a04c22c56c` | `b6387e358b9fa3b26b1253ca8d19050c6d6582a4` | `e3ed01f887449258bc7b4307cf0160472fe8b6c3` |
| Red | `e25c954ef6fdb7830d089cb529d3122e554fbd7b` | `901b403c42eed59e985407a60d0fc88254940dbb` | `e3a7f9b82d19a1166afbe3bd75678330fab9408b` |
| Orange | `67c996cc2e2e5af5cd59e9a4ea521693096370bc` | `541fcffc7b2c3a17a386e4787733dc5b17b32378` | `a9a7d7ab5bec13e8d0580c9f2029cf6b65f1ca13` |
| Grey | `97e1c6fb2b071a83dbaf197ba25a214cf0ef0a55` | `1c983b8dbd7dc166da1bc020e40456f5c1d49c93` | `dca49157612adcb7cb4138c9edc4389b869d202f` |
| Purple | `c09fe6f42b2ee25ce781bc0cf29eaf4469a335cc` | `1ea3aff575f3fa55c63b6b27952f104fdcc46873` | `bac9e7bb8bcb17fb6c52437a70449bece0a66166` |

### Progress bar
```js
const track = mkF(parent, { dir: 'HORIZONTAL', gap: 0, radius: 4, bg: V.borderDefault });
track.resize(400, 8); track.clipsContent = true;
const fill = figma.createRectangle(); fill.resize(pct * 4, 8);
setFill(fill, V.theme1); track.appendChild(fill);
```

---

## Gotchas & Lessons Learned

1. **Variant switching via `getComponentSetAsync()`** can throw "not a function" — safer to import a different component type directly.
2. **Alerts text override** — heading text node has no consistent name. Use `findAll(TEXT).find(n => n.characters?.includes('Alert'))`.
3. **AttentionBox body text** — Use `setLongText()` helper to find the first text node with >20 characters.
4. **Import only needed vars** — When continuing a partial build, import only the VK entries you need to save execution time.
5. **Container defaults to HORIZONTAL** after layout clone — always set `layoutMode='VERTICAL'` explicitly.

---

## Reference Files

| File | Contains |
|---|---|
| `docs/zcatalyst-design-system.md` | 59 component sets + Layout component with keys, variants, props, text node names |
| `docs/zcatalyst-styles.md` | 26 text styles + 500+ color variables with keys |
| `.github/copilot-instructions.md` | Full workflow auto-loaded by Copilot (clone, vars, helpers, patterns) |
