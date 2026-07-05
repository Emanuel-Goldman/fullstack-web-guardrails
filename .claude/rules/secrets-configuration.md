---
paths:
  - "frontend/**/*"
  - "backend/**/*"
  - "firebase.json"
  - ".firebaserc"
  - ".github/workflows/**/*.{yml,yaml}"
---

# Secrets and Configuration Rule

- Never commit secrets, private keys, tokens, production credentials, or populated environment files.
- Treat frontend environment variables as public because they are bundled into client code.
- Keep server secrets in an approved secret manager or protected deployment environment, not source code.
- Provide a safe `.env.example` containing names and documentation but no secret values.
- Validate required backend configuration at startup with a typed settings layer.
- Keep local, test, staging, and production configuration separate and explicit.
- Use the normal Firebase web configuration in the frontend only with restrictive Security Rules and authorized-domain settings; it is not a substitute for authorization.
- Rotate and revoke a credential immediately if it is exposed.
