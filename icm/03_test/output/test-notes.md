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

## Baseline

Focus background still requests `assets/focus-bg.jpg`, which is not in git. The contact `onsubmit` handler still throws `Unexpected identifier 'll'` on the apostrophe. That string is unchanged from `main`.
