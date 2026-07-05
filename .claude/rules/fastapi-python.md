---
paths:
  - "backend/**/*.py"
---

# FastAPI and Python Rule

- Use FastAPI for HTTP endpoints and Pydantic models for validated request and response schemas.
- Add Python type hints to public functions, service boundaries, dependencies, and return values.
- Keep route handlers thin: validate and authorize at the boundary, then delegate business logic to services.
- Use FastAPI dependency injection for authentication, configuration, and replaceable service dependencies.
- Use `async def` only when awaiting non-blocking I/O; do not call blocking libraries from the event loop.
- Return deliberate HTTP status codes and stable error shapes; do not expose raw internal exceptions.
- Keep database and Firebase Admin SDK access behind focused repository or service interfaces.
- Follow the project's formatter, linter, and type-checker settings; for new projects prefer Ruff and a configured static type checker.
