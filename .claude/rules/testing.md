---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "frontend/**/*.{test,spec}.{ts,tsx}"
  - "backend/**/*.py"
  - "firestore.rules"
---

# Testing Rule

- Add or update tests whenever behavior changes or a bug is fixed.
- Test observable behavior and contracts rather than private implementation details.
- Use Vitest and React Testing Library for frontend unit and component tests.
- Prefer user-centered queries such as role, label, and visible text over test IDs or CSS selectors.
- Use pytest with FastAPI `TestClient` or HTTPX for backend routes, services, validation, authentication, and error cases.
- Test Firestore and Authentication integration against the Firebase Local Emulator Suite, never production data.
- Test Firestore Security Rules with `@firebase/rules-unit-testing`, including both allowed and denied operations.
- Mock only external boundaries; avoid mocks that merely repeat the implementation.
- Keep tests deterministic, isolated, and safe to run in any order.
- Do not call work complete while relevant tests, type checks, or builds are failing.
