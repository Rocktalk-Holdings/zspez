# Change log — orange on black

## Edited

- `index.html` `:root` holds the `--z-*` brand tokens. Filled CTAs, focus rings, selection, and small accents use `--z-acc` (`#fd6d01`). Text on orange fills uses `--z-acc-ink`.
- Header "Get in touch" is a ghost control: transparent fill, `#6d6d71` border, `#e6e6e6` text. Orange only on hover and when that section is current. The hero "Start a conversation" is the only filled orange CTA in the first view.
- Nav links are `#e6e6e6`. Footer links and the email are `#9e9e9e`. Both turn `#fd6d01` on hover and on the current section.
- Hero and Values orange glow blobs are removed.
- Hero slides point at `assets/hero-101.png` through `assets/hero-404.png`.
- Focus ring is `2px solid #fd6d01` with `outline-offset: 3px`.
- Copyright line is exactly `© 2026 Zspez LLC`.
- Focus cards no longer show a HOVER label. A dim arrow appears on hover and focus.
- At 360 the hero headline sits 36px under the header. Carousel dots sit below the frame, each with a 44px hit area.
- `#services`, `#focus`, `#values`, and `#contact` use `scroll-margin-top: 72px`. The header background is solid `#141416` with a bottom border.
- `scripts/check-no-purple` scans source and any build directory for purple and violet hues.
- `scripts/check-landing` checks the copyright string, the ghost header, and a single filled hero CTA.
- Header side inset matches the 24px content gutter at every width. "Get in touch" keeps 16px of inner side padding.
- Long words and the contact field shrink inside the viewport at 200% zoom and 200% text. The nav row can wrap. Carousel dots can wrap. Under 220px the value number sits above its title so the card padding fits.
- The contact form still only calls `preventDefault`. The thanks state now runs, because the apostrophe lived in the page script instead of a broken attribute string.
- Page content after the header sits in `<main>`. Footer group labels are paragraphs, so heading levels do not skip.
- Focus background `src` is `assets/focus-bg.png`, covered by a 90% `--z-bg` scrim. `onerror` stays.

## Refused

- Did not move `index.html` or `assets/`.
- Did not delete `onerror`.
- Did not add a form backend.
- Did not add a color for the eyebrow or subtitle. Measured pairs already clear 4.5:1.
