---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# Small Functions Rule

- Give each function one clear responsibility and a name that describes its result or effect.
- Keep orchestration separate from calculations, validation, persistence, and presentation.
- Extract a helper when a block has a meaningful name, is reused, or can be tested independently.
- Do not split straightforward logic into tiny indirections that make the call flow harder to follow.
- Prefer explicit parameters and return values over hidden module state or mutation.
- Keep functions short enough that their assumptions, branches, and failure modes can be understood together.
