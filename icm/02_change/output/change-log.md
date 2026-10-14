# Change log — orange on black

## Edited

- `index.html` `:root` holds the `--z-*` brand tokens. Filled CTAs, focus rings, selection, and small accents use `--z-acc` (`#fd6d01`). Text on orange fills uses `--z-acc-ink`.
- Header "Get in touch" is a ghost control: transparent fill, `#6d6d71` border, `#e6e6e6` text. Orange only on hover and when that section is current. The hero "Start a conversation" is the only filled orange CTA in the first view.
- Nav links are `#e6e6e6`. Footer links and the email are `#9e9e9e`. Both turn `#fd6d01` on hover and on the current section.
- Hero and Values orange glow blobs are removed.
- Hero slides point at `assets/hero-101.png` through `assets/hero-404.png`.
- Focus ring is `2px solid #fd6d01` with `outline-offset: 3px`.
- Copyright line is exactly `© 2026 Zspez LLC`.
- `scripts/check-no-purple` scans source and any build directory for purple and violet hues.
- `scripts/check-landing` checks the copyright string, the ghost header, and a single filled hero CTA.

## Refused

- Did not move `index.html` or `assets/`.
- Did not delete `onerror`.
- Did not add a form backend or change the contact handler.
- Did not add a color for the eyebrow or subtitle. Measured pairs already clear 4.5:1.
- Did not retarget `assets/focus-bg.jpg`. That file is still absent.
