---
type: object
cluster: media
universe: live
status: verified
verified: 2026-09-20
commit: 1023111
entity: assets/
---

# Image assets = `assets/*.png`

Hero carousel and focus background `src` values point at the PNG files in git.

## Why this shape

The page is static. Images are just files next to `index.html`. The 2026-09-04 commit hid missing JPGs with `onerror` instead of retargeting `src`.

## Shape

| HTML `src` | File in git |
|---|---|
| `assets/hero-101.png` | `assets/hero-101.png` |
| `assets/hero-202.png` | `assets/hero-202.png` |
| `assets/hero-303.png` | `assets/hero-303.png` |
| `assets/hero-404.png` | `assets/hero-404.png` |
| `assets/focus-bg.png` | `assets/focus-bg.png` |

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
