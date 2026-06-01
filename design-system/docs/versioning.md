# Versioning

This library follows [Semantic Versioning](https://semver.org/) — the industry standard for design systems.

## Version Format

```
v MAJOR . MINOR . PATCH
```

| Segment | When to increment | Example change |
|---------|------------------|----------------|
| **PATCH** `v0.0.x` | Bug fixes, optimisations, no breaking changes | Fix incorrect border-radius token value |
| **MINOR** `v0.x.0` | New features, new tokens, non-breaking additions or tweaks | Add `color-background-warning` token |
| **MAJOR** `vx.0.0` | Breaking changes — renames, removals, structural shifts | Rename `--color-blue` → `--color-background-brand` |

## Pre-release (`v0.x.x`)

A `0.x` major version signals the library is **emerging** — it may be unstable or subject to significant changes. Consumers should pin to an exact version and review the CHANGELOG carefully before upgrading.

Once the system is stable and adopted across all primary teams, it will graduate to `v1.0.0`.

## Change Log

Every release must include a CHANGELOG entry following [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format:

```markdown
## [0.2.0] — YYYY-MM-DD

### Added
- New `color-background-warning` semantic token

### Changed
- Increased `--nav-height` from 56px to 60px

### Fixed
- Corrected `--shadow-md` value

### Removed
- Deprecated `--color-blue` (use `--color-background-brand`)
```

## Communicating Changes

- Post to the design system Slack channel on every release
- Tag consuming teams on breaking changes with a migration guide
- Maintain a CHANGELOG page in the documentation site (Zeroheight or equivalent)
