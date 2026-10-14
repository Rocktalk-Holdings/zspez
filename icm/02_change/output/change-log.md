# Change log — orange on black

## Edited

- `index.html` `:root` now holds only the `--z-*` brand tokens. CTAs, links, focus rings, selection, and highlights use `--z-acc`. Text on orange fills uses `--z-acc-ink`.
- Surfaces that sat behind orange text moved onto `--z-bg`, `--z-surface`, `--z-surface-2`, and `--z-tile` so the orange meets WCAG AA. No color outside the token list was added.
- Inline SVG diagrams use those same tokens. `theme-color` is `#0b0b0c` (`--z-bg`).
- `scripts/check-no-purple` scans source and, when present, `dist`, `build`, `out`, `_site`, `public`, and `site`. This repo has no build directory; the static root is the publishable output.
- Token and host citations: `icm/_shared/brand.md`, `icm/map/objects/landing-page.md`, `icm/map/processes/serve-and-browse.md`.

## Refused

- Did not move `index.html` or `assets/`.
- Did not retarget image `src` or delete `onerror`.
- Did not add a form backend or change the contact handler.
- Did not import the zspez.ai mark SVG. That file uses oranges and blues outside this token list.
- Did not add a package manifest or a second catalog.
