---
type: change-note
status: approved
universe: live
---

# Change note

## Request

Fix the off-brand purple on the Zspez landing page. The brand is orange on black. Replace every purple with the live zspez.ai tokens (`--z-bg` through `--z-ok`). Use `--z-acc` for CTAs, links, focus, and highlights, and `--z-acc-ink` for text on orange fills. Add no other colors. Keep text at WCAG AA and focus rings at 3:1. Add `scripts/check-no-purple`, run it, and screenshot the built page at 360, 393, and 1440.

## Universe

live

## Surfaces

- `index.html` — `:root` tokens, hover and focus, SVG fills, `theme-color`
- `scripts/check-no-purple` — hue scan of source and publishable output
- `icm/_shared/brand.md` — token pointer
- `icm/map/objects/landing-page.md` — token citation
- `icm/map/processes/serve-and-browse.md` — host found while checking deploy

## Hits / Does not hit

- **Hits:** `:root` tokens and every component that used them (landing page). Host note on serve-and-browse.
- **Does not hit:** image bytes, `src=` paths, form backend, carousel timer, copy, legal name, address, email.

## Verify

`scripts/check-no-purple`. Playwright on `http://127.0.0.1:8080/` at 360, 393, and 1440, before and after. Text contrast and focus-ring contrast on the built page.

## Human gate

Phone review: orange on black, no purple, address and email unchanged, photos still the known missing-JPG baseline. Do not merge until that read.
