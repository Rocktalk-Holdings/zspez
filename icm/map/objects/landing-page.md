---
type: object
cluster: page
universe: live
status: verified
verified: 2026-09-20
commit: 1023111
entity: index.html
---

# Landing page = `index.html`

The whole public site is one HTML file: tokens, sections, carousel script, and form handler.

## Why this shape

Clone-and-open. No bundler. A change to look, copy, or behavior is almost always a change to this file.

## Shape

- Tokens: `:root` `index.html:8-26`
- Sticky nav + in-page anchors: `index.html:551-564`
- Hero: `index.html:567-602`
- Method `#services`: `index.html:605-642`
- Focus `#focus`: `index.html:645-795`
- Values `#values`: `index.html:798-834`
- Contact `#contact`: `index.html:837-848`
- Footer: `index.html:851-874`
- Breakpoints at max-width 860 / 720 / 560 / 480
- `prefers-reduced-motion` kills carousel fade and flip (`index.html:184-186`, `index.html:493-496`)

## Connected to

- **owns:** [image-assets](image-assets.md), [contact-form](contact-form.md)
- **owned-by:** hosting that serves the repo root
- **joins:** `assets/` via `src=`
- **looks-like-but-is-not:** a multi-page or Markdown site — copy is HTML

## If you change this

- **Hits:** any section you edited; token changes hit every component that uses that variable; ID changes hit nav and footer `href`s
- **Does not hit:** PNG bytes in `assets/` unless you also change `src`; ICM contracts unless the map became wrong

## Surfaces

| Surface | Role |
|---|---|
| Browser | reads |
| Owner / agent | writes HTML |
| `icm/map` | cites, does not copy |

## See

- Source: `index.html`
- Impact: `../effects/CONTEXT.md`
