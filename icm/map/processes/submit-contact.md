---
type: process
status: verified
verified: 2026-09-20
commit: 1023111
consumes: [contact-form]
produces: []
---

# submit-contact

Validate the email field, cancel navigation, show thanks on the button.

## Input → Movement → Output

The visitor types an email and clicks Send. The browser `required` check runs. If valid, `preventDefault` fires and the button becomes a disabled thank-you. Refresh clears it. No payload is sent.

## Why this shape

A real `<form action>` would navigate away or 405 on a static host. The inline handler is the whole movement.

## Steps

1. `onsubmit` on `.cta-form` `index.html:842`.
2. `event.preventDefault()`.
3. Button text → `Thanks — we'll be in touch`; `disabled=true`.

## If you change this

- **Hits:** `#contact`, thanks copy, whether a host sees a POST
- **Does not hit:** footer mailto, carousel

## Surfaces

| Surface | Role |
|---|---|
| Visitor | submits |
| Inbox / API | none |

## See

- Objects: [contact-form](../objects/contact-form.md)
- Source: `index.html:842`
