---
type: process
status: verified
verified: 2026-09-20
commit: 1023111
consumes: [landing-page, image-assets]
produces: []
---

# serve-and-browse

Open the static file; the browser paints one document and jumps on hash links.

## Input → Movement → Output

A host or `file:` URL returns `index.html` (and `assets/` if `src` resolves). The browser applies CSS and runs the two scripts. The visitor sees sections and can hash-jump.

## Why this shape

There is no router, no `package.json`, and no documented production URL in-repo. Deploy is "serve the root."

## Steps

1. Client requests `/` or `index.html`.
2. Nav `href="#services|#focus|#values|#contact"` scrolls (`index.html:557-561`).
3. Images request the `src` paths; missing files fire `onerror` (`index.html:581`).

## If you change this

- **Hits:** how someone opens the site; hash targets; relative `assets/` URLs
- **Does not hit:** form thanks-state (that is submit-contact)

## Surfaces

| Surface | Role |
|---|---|
| Any static host | may serve this tree |
| `python3 -m http.server` | local proof |
| GitHub clone | source; not a host by itself |

## See

- Objects: [landing-page](../objects/landing-page.md), [image-assets](../objects/image-assets.md)
- Source: `index.html`
- Verify: `../../verify/CONTEXT.md`
