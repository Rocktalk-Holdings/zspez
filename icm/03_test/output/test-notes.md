# Test notes — orange on black

Viewport: Playwright Chromium, `prefers-reduced-motion: reduce`. Page opened at `http://127.0.0.1:8080/` (`python3 -m http.server 8080` from the repo root). There is no compile step.

## Commands

```bash
scripts/check-no-purple --self-test
scripts/check-no-purple
scripts/check-landing
```

Both checks exit 0. Purple scan: `violations: 0`. Landing check: copyright `© 2026 Zspez LLC`, one `.btn-primary` in the hero, header control is a ghost.

## Contrast (orange on tinted fills)

Text stayed `#fd6d01`. No lighter fill and no `#ff8a33`.

| Surface | Ratio |
|---|---|
| Services eyebrow on the 13% orange wash over `#141416` | 5.45:1 |
| Focus eyebrow on that wash over `#0b0b0c` | 5.97:1 |
| Values eyebrow on that wash over `#1b1b1e` | 5.04:1 |
| Contact eyebrow on that wash over `#141416` | 5.45:1 |
| Card subtitle on `#232327` | 5.49:1 |

## First view, buttons, illustrations

Filled orange control in the first 900px-tall view: only "Start a conversation", at 360, 393, and 1440.

Buttons (including carousel dots' hit area) are at least 44×44 CSS pixels. The header ghost is 44px tall. At 360 the four focus-card SVGs are about 217×174 and sit inside the cards.

Focus ring on the primary CTA: `rgb(253, 109, 1) solid 2px`, offset `3px`.

## Screenshots

- `/opt/cursor/artifacts/zspez-craft-360.png`
- `/opt/cursor/artifacts/zspez-craft-393.png`
- `/opt/cursor/artifacts/zspez-craft-1440.png`
- `/opt/cursor/artifacts/zspez-craft-360-hero.png`
- `/opt/cursor/artifacts/zspez-craft-360-focus.png`
- `/opt/cursor/artifacts/zspez-craft-360-focus-ring.png`

Earlier before/after shots from the purple pass are still in that folder.

## Pass 3 — labels, spacing, dots, sticky header

`scripts/check-no-purple` and `scripts/check-landing` both exit 0. Visible copy has no HOVER, lorem, TODO, or placeholder text.

At 360 the gap from the header bottom to the hero headline is 36px. Carousel dots sit below the frame (image bottom 993, dot top 997) and each hit target is 44×44. Header background is `rgb(20, 20, 22)` with a 1px solid bottom border.

Hash scroll to `#focus` at 360, with smooth scroll turned off so the shot is the settled viewport: `scrollY` 2503, section top 72, header bottom 73, first card top 444. The heading and the card clear the header. The screenshot is 360×800, the viewport, not a stitched full page.

Hover on the first Focus card shows the corner arrow (`::after` opacity 1). The other cards have no HOVER label.

Screenshots:

- `/opt/cursor/artifacts/zspez-pass3-360.png`
- `/opt/cursor/artifacts/zspez-pass3-1440.png`
- `/opt/cursor/artifacts/zspez-pass3-360-hero.png`
- `/opt/cursor/artifacts/zspez-pass3-360-focus-hover.png`
- `/opt/cursor/artifacts/zspez-pass3-360-header-scroll.png`

## Baseline

Focus background still requests `assets/focus-bg.jpg`, which is not in git. The contact `onsubmit` handler still throws `Unexpected identifier 'll'` on the apostrophe. That string is unchanged from `main`.
