---
type: object
cluster: contact
universe: live
status: verified
verified: 2026-09-20
commit: 1023111
entity: index.html
---

# Contact form = `#contact` (not mail)

An email field and Send button. Submit is cancelled in the browser. Nothing is stored or emailed.

## Why this shape

The page has no backend. The visible "thanks" state is the whole product. Real mail is the footer `mailto:` only.

## Shape

- Section `#contact` `index.html:837-848`
- `required` email input `#email`
- `onsubmit` `preventDefault`, then set button text to `Thanks — we'll be in touch` and `disabled=true` (`index.html:842`)
- Footer mail: `mailto:hello@zspez.com` `index.html:867` — **looks-like-but-is-not** this form

Ghost: any POST, inbox, or CRM. There is no action URL.

## Connected to

- **owns:** none
- **owned-by:** [landing-page](landing-page.md)
- **joins:** hero "Start a conversation" → `#contact`
- **looks-like-but-is-not:** footer mailto

## If you change this

- **Hits:** CTA section, thanks state, native `required` validation
- **Does not hit:** carousel, flip cards, image `src` mismatch

## Surfaces

| Surface | Role |
|---|---|
| Visitor | types, clicks |
| Server | none |
| Owner inbox | only if they click the footer mailto |

## See

- Source: `index.html:837-848`
- Process: `../processes/submit-contact.md`
