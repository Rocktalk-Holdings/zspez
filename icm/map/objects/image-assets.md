---
type: object
cluster: media
universe: live
status: verified
verified: 2026-09-20
commit: 1023111
entity: assets/
---

# Image assets = `assets/`

Hero carousel `src` values point at original SVG files. The focus section is a flat `#0b0b0c` band. `assets/ASSETS.md` records the source and license of each file.

## Why this shape

The page is static. Images are just files next to `index.html`. The 2026-09-04 commit hid missing JPGs with `onerror` instead of retargeting `src`.

## Shape

| HTML `src` | File in git |
|---|---|
| `assets/hero-laptop.svg` | `assets/hero-laptop.svg` |
| `assets/hero-monitor.svg` | `assets/hero-monitor.svg` |
| `assets/hero-phone.svg` | `assets/hero-phone.svg` |
| `assets/hero-tablet.svg` | `assets/hero-tablet.svg` |

Leftover: `onerror="this.style.display='none'"` on those `<img>` tags.

## Connected to

- **owns:** none
- **owned-by:** [landing-page](landing-page.md)
- **joins:** carousel process, focus section background
- **looks-like-but-is-not:** the carousel JS — JS only toggles `.is-active`

## If you change this

- **Hits:** hero frame, focus backdrop, `onerror` behavior
- **Does not hit:** card copy, form handler, footer address

## Surfaces

| Surface | Role |
|---|---|
| Browser | requests `src`, hides on error |
| Owner | drops new files into `assets/` |
| Outside host / CDN | none in-repo |

## See

- Source: `assets/`, `index.html:581-591`, `index.html:647`
- Process: `../processes/rotate-carousel.md`
