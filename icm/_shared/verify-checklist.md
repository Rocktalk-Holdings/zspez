# Verify checklist

Use with `icm/verify/CONTEXT.md`. Check only the rows the change can hit.

1. Open the page (local server or `index.html` in a browser).
2. Nav jumps: Our Method, Our Focus, Our Values, Get in touch.
3. Hero: headline, two buttons, carousel dots (click + auto-advance if motion is on).
4. `#services`: three cards visible on a wide window; stack on a narrow one.
5. `#focus`: four flips — hover or keyboard focus; background still sits behind.
6. `#values`: four items; dark panel readable.
7. `#contact`: valid email → button reads `Thanks — we'll be in touch` and disables. Invalid email → native required prompt.
8. Footer: address, in-page links, `build@zspez.ai`.
9. Narrow viewport (~400px): nav CTA remains; body cards stack; form stacks.
10. `prefers-reduced-motion`: carousel does not auto-play; flips do not rotate.

Images: HTML `src` values are `assets/hero-laptop.svg`, `hero-monitor.svg`, `hero-phone.svg`, and `hero-tablet.svg`. `onerror` still hides an image if a file is missing. The street address is `7301 W 129th St, Overland Park, KS 66213`.
