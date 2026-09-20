---
type: process
status: verified
verified: 2026-09-20
commit: 1023111
consumes: [image-assets]
produces: []
---

# rotate-carousel

Cycle `.carousel-slide` active state every 5s, or on dot click.

## Input → Movement → Output

The script finds `[data-carousel]`. It toggles `.is-active` on slides and dots. Reduced motion skips the timer.

## Why this shape

No library. If you "just swap a slider component" you drop pause-on-hover, tab-hidden pause, and the reduced-motion branch.

## Steps

1. IIFE binds `[data-carousel]` `index.html:499-545`.
2. `go(n)` sets `.is-active` and `aria-selected` `index.html:515-522`.
3. `setInterval` 5000ms unless `prefers-reduced-motion` `index.html:513-528`.
4. Dots click → `go(i)` and restart; hover and `visibilitychange` pause `index.html:531-542`.

## If you change this

- **Hits:** hero visual, dots, autoplay, a11y selected state
- **Does not hit:** focus flip cards (separate CSS), contact form

## Surfaces

| Surface | Role |
|---|---|
| Visitor | sees / clicks dots |
| Agent | edits the IIFE or markup |

## See

- Objects: [image-assets](../objects/image-assets.md), [landing-page](../objects/landing-page.md)
- Source: `index.html:499-545`, `index.html:578-599`
