# Accessibility Guidelines

## Principles

All components must meet **WCAG 2.1 AA** as a minimum. Target AAA where feasible.

## Colour Contrast

| Use case | Minimum ratio |
|----------|---------------|
| Normal text (< 18px) | 4.5:1 |
| Large text (≥ 18px or ≥ 14px bold) | 3:1 |
| UI components & graphical objects | 3:1 |
| Decorative elements | No requirement |

Token pairings that pass AA:

| Text token | Background token | Ratio |
|-----------|-----------------|-------|
| `--color-text-strong` (#101c2f) | `--color-background-default` (#fff) | 18.6:1 ✅ |
| `--color-text-default` (#3f4d62) | `--color-background-default` (#fff) | 8.1:1 ✅ |
| `--color-text-inverse` (#fff) | `--color-background-brand` (#0066cc) | 4.6:1 ✅ |
| `--color-text-inverse` (#fff) | `--color-background-inverse` (#101c2f) | 18.6:1 ✅ |

## Focus Management

- All interactive elements must have a **visible focus indicator**
- Use `--focus-ring` for standard focus, `--focus-ring-inset` for elements inside bordered containers
- Never use `outline: none` without providing an equivalent custom focus style
- Focus must follow a **logical tab order** — do not use `tabindex > 0`

## Keyboard Navigation

| Component | Expected behaviour |
|-----------|-------------------|
| Nav dropdowns | `Enter`/`Space` opens; `Escape` closes; arrow keys move between items |
| FAQ accordion | `Enter`/`Space` toggles; `Escape` collapses |
| Modal / Drawer | Focus trapped inside while open; `Escape` closes; focus returns on close |
| Search overlay | Focus moves to input on open; `Escape` closes |

## ARIA

- Use semantic HTML first — only add ARIA when HTML semantics are insufficient
- `aria-expanded` on all toggle triggers
- `aria-haspopup` on nav items that open mega panels
- `aria-controls` to associate triggers with their panels
- `aria-label` on icon-only buttons (search, language, close)
- `role="dialog"` + `aria-modal="true"` on drawers and modals
- `aria-hidden="true"` on decorative icons

## Motion

Respect `prefers-reduced-motion`:

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```
