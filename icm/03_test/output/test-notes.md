# Test notes — orange on black

Viewport: Playwright Chromium, `prefers-reduced-motion: reduce`, full page at 360, 393, and 1440. Page opened at `http://127.0.0.1:8080/` (`python3 -m http.server 8080` from the repo root). There is no compile step; that URL is the built page.

## Commands

```bash
python3 -m http.server 8080
scripts/check-no-purple --self-test
scripts/check-no-purple
```

Checker: self-test ok. Scan found `index.html` only, no `dist`/`build`/`out`/`_site`/`public`/`site`, `violations: 0`, exit 0.

## Screenshots

Before (purple on a light page) and after (orange on black):

- `/opt/cursor/artifacts/zspez-before-360.png`
- `/opt/cursor/artifacts/zspez-before-393.png`
- `/opt/cursor/artifacts/zspez-before-1440.png`
- `/opt/cursor/artifacts/zspez-after-360.png`
- `/opt/cursor/artifacts/zspez-after-393.png`
- `/opt/cursor/artifacts/zspez-after-1440.png`
- `/opt/cursor/artifacts/zspez-after-1440-focus-cta.png` (keyboard-style focus on the primary CTA)

## Checklist rows this change can hit

| Row | Result |
|---|---|
| Page opens | Pass — HTTP 200 |
| Tokens / sections | Pass — full-page shots at 360, 393, 1440. Hero, method, focus, values, contact, footer all use the dark tokens. Narrow widths stack cards; nav CTA stays. |
| Text contrast | Pass — sampled pairs 5.45:1 to 19.67:1 (AA is 4.5:1). Lowest is the orange eyebrow on the soft orange wash. |
| Focus rings | Pass — Tab order shows `3px solid rgb(253, 109, 1)` with `outline-offset: 3px`. Orange against `#0b0b0c` is 6.90:1 (need 3:1). |
| Rendered purple | Pass — every computed color on the page was outside the purple hue band. `theme-color` is `#0b0b0c`. Selection is orange fill with `#140700` text. |
| Invalid email border | Pass — `user-invalid` border is `rgb(255, 138, 122)` (`--z-err`). Button label stays `Send`. |
| Images | Baseline unchanged. HTML still names missing JPGs; `onerror` still hides them. |
| Address, email, legal name | Unchanged |

## Failures

None in this diff. The contact `onsubmit` handler still throws `Unexpected identifier 'll'` because of the apostrophe escape. That string is unchanged from `main`. Valid submit does not reach the thanks label. Not introduced here.
