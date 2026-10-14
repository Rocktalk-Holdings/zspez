# Test notes — inbox and hero art

Page: `http://127.0.0.1:8080/` from `python3 -m http.server 8080` at the repo root. Playwright Chromium.

## Commands

```bash
scripts/check-no-purple --self-test
scripts/check-no-purple
scripts/check-landing
```

Both checks exit 0. Purple scan: `violations: 0` (the four SVGs are included). Landing check prints `inbox: build@zspez.ai`.

## Checklist rows this change can hit

| Row | Result |
|---|---|
| Footer mailto is `mailto:build@zspez.ai` and the visible text matches | Pass at 320, 360, 768, 1024, 1440, 1920 |
| No horizontal scroll | Pass at those widths. At 320 the address box ends at 296, inside the 24px gutter |
| Carousel dots | 44×44. Reduced motion stays on `hero-laptop.svg` after 1.2s |
| Broken hero image | Aborting SVG requests hides the slides and does not widen the page |
| Form | Unchanged handler. Not the inbox |
| Address and copyright | Unchanged |

axe-core at 360 and 1440: no violations.

## Craft follow-up

At 360, scrollY 0, the header box is top 0, height 73, sticky, margin 0. Its parent `body` has margin 0 and transform none. The first pixel row of the viewport screenshot is the header color `#141416`.

H1 bounding box at 360×800: x 24, y 109, width 312, height 176.625, right 336, bottom 285.625. The text is `We turn emerging tech into everyday tools.` The box starts 36px below the header and ends inside the viewport, so the headline is fully visible.

The Send button's platform font is Noto Sans Bold. Four slides and four dots remain. The focus section background is `rgb(11, 11, 12)`. The hero frame border width is 0. The address text is `7301 W 129th St, Overland Park, KS 66213`. axe-core reports no violations at 360 and 1440. Both check scripts exit 0.

## Screenshots

- `/opt/cursor/artifacts/zspez-craft4-1440.png` — full page at 1440
- `/opt/cursor/artifacts/zspez-craft4-360-top.png` — top of the page at 360, viewport only
- `/opt/cursor/artifacts/zspez-craft4-360-contact.png` — contact area at 360
