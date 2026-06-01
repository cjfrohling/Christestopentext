# Naming Conventions

## Principle

Token names must be **clear, fully written out, and predictable**. Abbreviations make the system confusing and hard to use across tools and environments.

```
✅ color-background-brand-knockout-hover
🚫 color-bg-br-kn-hv
```

## Token Name Structure

```
[category]-[property]-[variant]-[state]
```

| Segment | Description | Example |
|---------|-------------|--------|
| category | The design property type | `color`, `typography`, `spacing`, `border`, `shadow` |
| property | What it applies to | `background`, `text`, `border`, `radius` |
| variant | Semantic role or scale | `brand`, `default`, `subtle`, `strong`, `knockout` |
| state | Interaction state (optional) | `hover`, `active`, `disabled`, `focus` |

## Examples

```css
/* Colour */
--color-background-default
--color-background-default-hover
--color-background-subtle
--color-background-knockout
--color-background-brand
--color-background-brand-hover

/* Text */
--color-text-strong
--color-text-default
--color-text-subtle
--color-text-disabled
--color-text-inverse
--color-text-brand

/* Border */
--color-border-default
--color-border-brand
--color-border-inverse

/* Spacing */
--spacing-component-sm
--spacing-layout-lg

/* Typography */
--typography-h1-size
--typography-body-md-weight
```

## Component Tokens (Tier 3)

Component tokens follow the same pattern, prefixed by the component name:

```css
--button-background
--button-background-hover
--button-text
--button-border-radius

--field-border
--field-border-focus

--nav-height
--nav-item-text-active
```

## Rules

1. **No abbreviations** — write words in full
2. **Lowercase kebab-case** throughout
3. **Be predictable** — follow the algorithm above
4. **No hard-coded values** in components — always reference a token
5. **Tier 3 sparingly** — prefer Tier 2 semantic tokens unless variation is truly component-specific
