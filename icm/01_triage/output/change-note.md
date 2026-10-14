---
type: change-note
status: proceed
universe: live
---

# Change note

## Request

Replace every hello@zspez.com on the landing page with build@zspez.ai, covering mailto links, visible text, meta tags, form handlers, and JS. Add a check to scripts/check-landing that fails on any zspez.com email address and requires build@zspez.ai.

Drew approved replacing hero-101 through hero-404. Draw new original hero graphics in the zspez.ai tokens, delete the old files, record source and license in assets/ASSETS.md, and fail the landing check if those old names are referenced or an asset is missing from the manifest.

Open a new draft PR from latest main. Do not merge.

## Universe

live

## Surfaces

- `index.html` — footer mailto and the four hero `src` values
- `assets/hero-laptop.svg`, `hero-monitor.svg`, `hero-phone.svg`, `hero-tablet.svg` — new original graphics
- `assets/ASSETS.md` — source and license for every file in `assets/`
- `scripts/check-landing` — inbox rule, old hero names, asset manifest
- `icm/map/objects/contact-form.md`, `icm/map/objects/image-assets.md`, `icm/CONTEXT.md`, `icm/map/effects/CONTEXT.md`, `icm/_shared/verify-checklist.md` — citations of the inbox and the hero files

## Hits / Does not hit

- **Hits:** footer mailto, landing-page footer copy, contact-form's "looks like but is not" mail line
- **Does not hit:** form POST (still none), hero copy, images, tokens, street address, copyright

## Verify

`scripts/check-no-purple` and `scripts/check-landing`. Open `http://127.0.0.1:8080/`. Confirm the mailto, no horizontal scroll at 320 and 360, axe clean, screenshots of the 1440 page and the 360 contact and footer.

## Human gate

The only new sentence is `build@zspez.ai`. No folder move, no form backend. Draft PR, do not merge.
