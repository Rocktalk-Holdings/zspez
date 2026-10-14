# Change log — inbox and hero art

## Edited

- `index.html` footer mailto and visible address are `build@zspez.ai`. No other `zspez.com` email was on the page.
- Hero slides point at `assets/hero-laptop.svg`, `hero-monitor.svg`, `hero-phone.svg`, and `hero-tablet.svg`. Those files are hand-authored SVG in the existing tokens (`#fd6d01` on `#0b0b0c` and the other `--z-*` surfaces). Dots stay 44px. Reduced motion and `onerror` are unchanged.
- Deleted `assets/hero-101.png`, `hero-202.png`, `hero-303.png`, and `hero-404.png`.
- `assets/ASSETS.md` records source and license for every file in `assets/`, including `focus-bg.png`.
- `scripts/check-landing` fails on a `zspez.com` email, requires `mailto:build@zspez.ai` and the visible address, fails if `hero-101` … `hero-404` are referenced or still on disk, and fails if an asset file is missing from `ASSETS.md`.

## Refused

- Did not add a form backend.
- Did not delete `onerror`.
- Did not replace `focus-bg.png`. Its license is still unrecorded; the manifest says so.
- Did not use generated or stock imagery.
