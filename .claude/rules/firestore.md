---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
  - "firestore.indexes.json"
---

# Cloud Firestore Rule

- Design collections and documents around actual query patterns; Firestore is not a relational database.
- Keep document shapes explicit and validate data read from Firestore before using it as trusted application state.
- Store timestamps as Firestore timestamps and define clearly whether they are written by the client or server.
- Avoid unbounded reads and listeners; use filters, limits, cursors, and pagination.
- Use transactions or batched writes when correctness depends on atomic multi-document changes.
- Avoid sequential document IDs and single-document write hotspots in high-write paths.
- Add and version required composite indexes in `firestore.indexes.json`.
- Keep privileged writes on the FastAPI backend with the Firebase Admin SDK when client security rules cannot express the required policy safely.
- Account for read, write, storage, and listener costs when choosing a data model.
