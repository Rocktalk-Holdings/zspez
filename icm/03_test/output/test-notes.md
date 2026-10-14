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

## Screenshots

- `/opt/cursor/artifacts/zspez-inbox-1440.png` — full page, hero in the first view
- `/opt/cursor/artifacts/zspez-inbox-360-hero.png` — hero graphic at 360
- `/opt/cursor/artifacts/zspez-inbox-360-contact-footer.png` — contact through the footer, including `build@zspez.ai`
