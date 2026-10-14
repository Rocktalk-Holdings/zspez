# Verify checklist

Use with `icm/verify/CONTEXT.md`. Check only the rows the change can hit.

1. Open the page (local server or `index.html` in a browser).
2. Nav jumps: Our Method, Our Focus, Our Values, Get in touch.
3. Hero: headline, two buttons, carousel dots (click + auto-advance if motion is on).
4. `#services`: three cards visible on a wide window; stack on a narrow one.
5. `#focus`: four flips — hover or keyboard focus; background still sits behind.
6. `#values`: four items; dark panel readable.
7. `#contact`: valid email → button reads `Thanks — we'll be in touch` and disables. Invalid email → native required prompt.
8. Footer: address, in-page links, `hello@zspez.com`.
9. Narrow viewport (~400px): nav CTA remains; body cards stack; form stacks.
10. `prefers-reduced-motion`: carousel does not auto-play; flips do not rotate.

Images: HTML `src` values are `assets/hero-101.png` … `hero-404.png` and `assets/focus-bg.png`. `onerror` still hides an image if a file is missing.
