---
paths:
  - "frontend/src/**/*.{ts,tsx,css,scss}"
---

# Accessibility and Responsive UI Rule

- Use semantic HTML before adding ARIA roles or custom keyboard behavior.
- Give every interactive control an accessible name and ensure it is usable by keyboard.
- Associate form fields with labels and present validation errors in a way assistive technology can discover.
- Preserve visible focus indicators and sufficient color contrast.
- Use responsive layouts that work at narrow and wide viewport sizes without hiding essential actions.
- Respect reduced-motion preferences and avoid motion required to understand or operate the interface.
- Test meaningful user flows by role and accessible name rather than brittle CSS selectors.
