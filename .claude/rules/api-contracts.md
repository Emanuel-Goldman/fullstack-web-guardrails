---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# API Contract Rule

- Define request and response bodies with Pydantic models and expose accurate OpenAPI metadata.
- Treat the API schema as the contract between React and FastAPI.
- Generate TypeScript client types from OpenAPI when practical; do not let handwritten frontend types drift from backend schemas.
- Validate all untrusted data at the boundary, including path, query, header, body, and third-party response data.
- Use consistent JSON naming, timestamp, identifier, pagination, and error conventions.
- Make breaking contract changes explicit and update clients and tests in the same change.
- Do not return Firestore document snapshots or backend implementation objects directly from routes.
