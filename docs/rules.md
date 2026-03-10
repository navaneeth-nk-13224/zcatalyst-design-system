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

---

## Reference Files

| File | Contains |
|---|---|
| `docs/zcatalyst-design-system.md` | 59 component sets with keys, variants, props, text node names |
| `docs/zcatalyst-styles.md` | 26 text styles + 500+ color variables with keys |
