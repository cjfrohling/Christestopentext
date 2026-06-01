# OT BPv1 — Design System

OpenText Brand Patterns v1. A structured, token-driven design system covering tokens, components, patterns, and documentation guidelines.

## Library Structure

```
design-system/
├── tokens/
│   ├── primitives.css      # Tier 1 — raw values (colour palette, base spacing, font sizes)
│   ├── semantic.css        # Tier 2 — intent-mapped aliases (background, text, border)
│   └── component.css       # Tier 3 — component-specific overrides (use sparingly)
├── components/
│   ├── button/
│   ├── form/
│   ├── nav/
│   ├── card/
│   └── badge/
├── patterns/
│   ├── hero/
│   ├── mega-nav/
│   └── faq/
├── docs/
│   ├── governance.md
│   ├── naming-conventions.md
│   ├── accessibility.md
│   └── versioning.md
└── CHANGELOG.md
```

## Token Architecture

Three-tier token system:

| Tier | Name | Purpose | Example |
|------|------|---------|--------|
| 1 | Primitive | Raw values, never used directly in components | `--color-blue-600: #0066cc` |
| 2 | Semantic | Intent-mapped, used in most components | `--color-background-brand: var(--color-blue-600)` |
| 3 | Component | Scoped to a specific component, used sparingly | `--button-background: var(--color-background-brand)` |

## Getting Started

Import tokens in the correct order:

```html
<link rel="stylesheet" href="design-system/tokens/primitives.css">
<link rel="stylesheet" href="design-system/tokens/semantic.css">
<link rel="stylesheet" href="design-system/tokens/component.css">
```

## Versioning

This library follows [Semantic Versioning](https://semver.org/):
- **Patch** `v0.0.x` — bug fixes, no breaking changes
- **Minor** `v0.x.0` — new features or tokens, no breaking changes
- **Major** `vx.0.0` — breaking changes

See [CHANGELOG.md](./CHANGELOG.md) for release history.
