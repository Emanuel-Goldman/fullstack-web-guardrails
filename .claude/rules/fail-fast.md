---
paths:
  - "frontend/src/**/*.{ts,tsx}"
  - "backend/**/*.py"
---

# Fail-Fast Rule

- Validate required inputs at system boundaries: forms, API requests, environment configuration, and database documents.
- Reject invalid state with a clear, actionable error instead of silently applying a fallback that changes behavior.
- Do not catch broad exceptions unless adding useful context and re-raising or handling a specific expected failure.
- Treat impossible states as errors and make them unrepresentable with types or schemas when practical.
- Check required environment variables during application startup, not after the first affected request.
- Never ignore a failed network, database, authentication, build, test, or deployment operation.
