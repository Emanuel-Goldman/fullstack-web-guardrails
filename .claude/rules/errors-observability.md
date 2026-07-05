---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# Errors and Observability Rule

- Show users concise, actionable errors without exposing stack traces, credentials, internal paths, or database details.
- Preserve the original exception as the cause when adding backend context.
- Log structured context such as operation, request ID, actor ID when safe, and relevant resource identifiers.
- Never log passwords, authorization headers, ID tokens, session cookies, service-account keys, or sensitive document contents.
- Distinguish validation, authentication, authorization, not-found, conflict, dependency, and internal failures.
- Add frontend error boundaries around meaningful application regions and provide a recovery path.
- Use timeouts and deliberate retry policies for network calls; retry only failures that may safely succeed later.
- Make health and readiness behavior sufficient to diagnose deployment failures without revealing sensitive information.
