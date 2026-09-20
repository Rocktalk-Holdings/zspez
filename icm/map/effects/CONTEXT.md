# effects — if you change X

One job: name which cards to open. This file does not copy waterfalls. If it disagrees with a card, fix the card.

## Inputs

- Working (this run): the thing you are about to edit
- Reference (every run): the cards listed in that row only

Do NOT load: every object and process card.

## Process

1. Find your X.
2. Open those cards.
3. Edit the subject files they cite.

## Outputs

- A Hits / Does not hit answer you can paste into the triage note

## Human check

You opened two or fewer cards plus this index. If you needed more, the index row is too loose — split it.

## Index

| If you are changing | Open | Does not hit (wrong next noun) |
|---|---|---|
| Headline, method, focus, values, footer copy | [landing-page](../objects/landing-page.md) | [contact-form](../objects/contact-form.md) unless the CTA promise changed |
| `:root` tokens or breakpoints | [landing-page](../objects/landing-page.md) | [image-assets](../objects/image-assets.md) |
| Hero photos or `src=` | [image-assets](../objects/image-assets.md), [rotate-carousel](../processes/rotate-carousel.md) | [contact-form](../objects/contact-form.md) |
| Carousel timer, dots, reduced motion | [rotate-carousel](../processes/rotate-carousel.md) | focus `.flip` CSS |
| Flip cards or focus background | [landing-page](../objects/landing-page.md), [image-assets](../objects/image-assets.md) | [rotate-carousel](../processes/rotate-carousel.md) |
| Send button / thanks / email field | [contact-form](../objects/contact-form.md), [submit-contact](../processes/submit-contact.md) | footer mailto unless you change that too |
| How the site is opened or hosted | [serve-and-browse](../processes/serve-and-browse.md) | form POST (there is none) |
| ICM map / runbook only | the area `CONTEXT.md` | `index.html` |

## What points in from outside

Nothing in this repo names a production host. Outside consumers to ask the owner about: any live domain, GitHub Pages, a clone-and-deploy script, and inboxes that expect `hello@zspez.com`. Those break silently — record them on the card they land on when you learn them.
