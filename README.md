# Fullstack Web Guardrails

Reusable Claude Code rules for building maintainable, tested full-stack applications with React, TypeScript, FastAPI, Python, Firebase Hosting, and Cloud Firestore.

The collection combines general engineering guardrails—small functions, code reuse, clear naming, explicit errors—with stack-specific rules for React components, API contracts, Firestore security, automated tests, and production deployment.

## One-file quick start

Open [`CLAUDE-RULES.md`](CLAUDE-RULES.md), copy the entire file, and paste it into your project's `CLAUDE.md`.

Use the individual files under `.claude/rules/` when you prefer modular rules that apply only to matching paths.

## Opinionated stack

- Frontend: React and strict TypeScript
- Frontend build tooling: Vite for new standalone applications unless the project already uses another supported framework
- Backend: FastAPI and modern Python
- API schemas: Pydantic models and generated OpenAPI
- Database: Cloud Firestore
- Authentication: Firebase Authentication when authentication is required
- Frontend hosting: Firebase Hosting
- Backend hosting: Cloud Run, routed through Firebase Hosting when a shared origin is useful
- Frontend tests: Vitest and React Testing Library
- Backend tests: pytest and FastAPI `TestClient`/HTTPX
- Firebase integration tests: Firebase Local Emulator Suite and `@firebase/rules-unit-testing`

## Included rules

| Rule | Purpose |
| --- | --- |
| `fail-fast.md` | Expose invalid state and assumptions immediately. |
| `small-functions.md` | Keep functions focused, explicit, and easy to test. |
| `code-reuse.md` | Reuse established components, hooks, services, and schemas. |
| `clear-code.md` | Favor readable structure and domain language over cleverness. |
| `typescript.md` | Keep frontend code strictly and meaningfully typed. |
| `react-components.md` | Build focused, reusable, accessible React components. |
| `react-state-effects.md` | Keep state minimal and Effects synchronized with external systems. |
| `accessibility-responsive-ui.md` | Make interfaces accessible and usable across screen sizes. |
| `fastapi-python.md` | Structure typed, validated, idiomatic FastAPI services. |
| `api-contracts.md` | Keep frontend and backend contracts explicit and synchronized. |
| `firestore.md` | Model Firestore data intentionally and avoid costly access patterns. |
| `firebase-security.md` | Enforce authorization in rules and trusted backend code. |
| `firebase-deployment.md` | Deploy the frontend and FastAPI backend safely and repeatably. |
| `testing.md` | Require useful frontend, backend, and security-rule tests. |
| `errors-observability.md` | Provide safe user errors and actionable operational context. |
| `secrets-configuration.md` | Separate public configuration from server-side secrets. |
| `performance-dependencies.md` | Measure performance and keep dependencies deliberate. |

## Modular installation

PowerShell:

```powershell
Copy-Item -Recurse .claude\rules C:\path\to\your-project\.claude\rules
```

Bash:

```bash
cp -R .claude/rules /path/to/your-project/.claude/rules
```

Review the path scopes and adapt the rules to the structure and existing conventions of your project.

## Deployment model

Firebase Hosting serves the built React application. The FastAPI service runs as a container on Cloud Run; Firebase Hosting can rewrite `/api/**` requests to that service. Firestore and Firebase Authentication should be exercised locally through the Emulator Suite before production deployment.

Useful official references:

- [React with TypeScript](https://react.dev/learn/typescript)
- [FastAPI testing](https://fastapi.tiangolo.com/tutorial/testing/)
- [Firebase Hosting with Cloud Run](https://firebase.google.com/docs/hosting/cloud-run)
- [Firebase Local Emulator Suite](https://firebase.google.com/docs/emulator-suite)
- [Testing Firestore Security Rules](https://firebase.google.com/docs/firestore/security/test-rules-emulator)

## Repository structure

```text
.
|-- .claude/
|   `-- rules/
|       `-- *.md
|-- CLAUDE.md
|-- CLAUDE-RULES.md
|-- LICENSE
`-- README.md
```

## Contributing

Contributions are welcome. Keep additions concise, actionable, and tied to a concrete engineering, security, testing, or deployment failure they prevent.

## License

MIT
