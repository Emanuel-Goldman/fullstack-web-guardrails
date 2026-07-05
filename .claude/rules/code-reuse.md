---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# Code Reuse Rule

- Search for an existing component, hook, utility, service, dependency, or schema before adding a duplicate.
- Keep one authoritative implementation of business rules and validation logic.
- Reuse composition before introducing inheritance or a broad framework abstraction.
- Parameterize real variations instead of copying entire components, routes, or services.
- Share API types through generated clients or an explicit contract workflow rather than manually maintaining look-alike interfaces.
- Do not create a generic abstraction until multiple concrete use cases demonstrate the shared behavior.
