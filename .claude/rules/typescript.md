---
paths:
  - "frontend/**/*.{ts,tsx}"
---

# TypeScript Rule

- Use TypeScript for frontend application code and keep strict compiler checks enabled.
- Do not use `any` to bypass modeling work; prefer a precise type or `unknown` followed by validation and narrowing.
- Type component props, hook results, service boundaries, and external data explicitly.
- Prefer discriminated unions for state with mutually exclusive cases such as idle, loading, success, and error.
- Avoid unsafe type assertions; validate runtime data before treating it as a trusted type.
- Use generated or shared API types when available and do not duplicate backend schemas by hand without a synchronization check.
- Keep types near their domain owner and export only types that are genuinely shared.
