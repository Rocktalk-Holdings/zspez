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

## Pass 4 — gutter, break-it, axe

`scripts/check-no-purple` and `scripts/check-landing` both exit 0.

At 360 the brand and the headline both start 24px from the left. The header "Get in touch" control has 16px inner side padding and its right edge is 24px from the viewport. Its fill is transparent over `#141416`; the label is `#e6e6e6`.

Playwright at 320, 360, 768, 1024, 1440, and 1920: no horizontal scroll at 1×, at CSS zoom 2, or with the root font at 32px. The same holds at 160 and 180, the layout width of a 320 and 360 viewport at 200% zoom. Keyboard Tab walks every control and lands on the document (no trap); each focused control shows a 2px solid orange outline. Shift+Tab moves back. Reduced motion keeps the laptop slide and does not flip a card. Aborting images hides them and leaves the headline. A delayed image does not block the headline or the hero CTA. An 80-character email stays inside the field. A valid submit reads `Thanks — we'll be in touch` and disables the button. An invalid email leaves the button as Send. Links are only `#`, `#services`, `#focus`, `#values`, `#contact`, and `mailto:hello@zspez.com`.

axe-core on the page at 360 and 1440: no violations. Before the landmark and heading fix it reported `heading-order`, `landmark-one-main`, and `region`, all moderate.

Screenshots:

- `/opt/cursor/artifacts/zspez-final-360-header.png`
- `/opt/cursor/artifacts/zspez-final-1440.png`
