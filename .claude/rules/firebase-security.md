---
paths:
  - "firestore.rules"
  - "storage.rules"
  - "firebase.json"
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# Firebase Security Rule

- Deny access by default in Firestore and Storage Security Rules, then grant only the minimum required operations.
- Treat client input and client-side role checks as untrusted; enforce authorization in Security Rules or trusted FastAPI code.
- Verify Firebase ID tokens on protected backend endpoints and derive identity from the verified token, never from a submitted user ID.
- Check resource ownership, allowed fields, data types, and immutable fields in Firestore Security Rules.
- Never use permissive production rules such as unconditional `allow read, write: if true`.
- Test allowed and denied operations with the Firebase Emulator Suite and `@firebase/rules-unit-testing`.
- Keep development, staging, and production Firebase projects separate.
- Do not expose service-account keys or Admin SDK credentials to frontend code.
