---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# Clear Code Rule

- Prefer descriptive domain names over abbreviations, generic labels, or implementation jargon.
- Make control flow obvious; use early returns to reduce nesting when they improve readability.
- Keep files centered on one feature or responsibility and follow the project's established structure.
- Comment why a non-obvious decision exists, not what plainly readable code does.
- Replace unexplained literals with named constants when the value carries domain meaning.
- Avoid hidden side effects, surprising mutation, and clever expressions that are difficult to debug.
- Preserve the existing formatter, linter, and import conventions rather than creating competing styles.
