---
type: object
cluster: media
universe: live
status: verified
verified: 2026-09-20
commit: 1023111
entity: assets/
---

# Image assets = `assets/*.png` (HTML still says `.jpg`)

Photos that should fill the hero carousel and the focus background. Files on disk and `src=` strings do not match.

## Why this shape

The page is static. Images are just files next to `index.html`. The 2026-09-04 commit hid missing JPGs with `onerror` instead of retargeting `src`.

## Shape

| HTML `src` (ghost) | File in git (live) |
|---|---|
| `assets/hero-1.jpg` `index.html:581` | `assets/hero-101.png` |
| `assets/hero-2.jpg` `index.html:584` | `assets/hero-202.png` |
| `assets/hero-3.jpg` `index.html:587` | `assets/hero-303.png` |
| `assets/hero-4.jpg` `index.html:590` | `assets/hero-404.png` |
| `assets/focus-bg.jpg` `index.html:647` | `assets/focus-bg.png` |

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
