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

### Status badge (green/red/orange)
```js
const badge = mkF(parent, { dir: 'HORIZONTAL', gap: 4, padX: 8, padY: 3, fillW: false, radius: 4, bg: V.green4, align: 'CENTER' });
const dot = figma.createEllipse(); dot.resize(6, 6); setFill(dot, V.green1); badge.appendChild(dot);
await mkText(badge, 'Active', '540b559794ca7eb23631093b727eddd1d41c14b7', V.green1);
```

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
