---
paths:
  - ".github/workflows/**/*.{yml,yaml}"
---

# GitHub Actions CI/CD Rule

- Define CI in GitHub Actions and run it for pull requests and pushes to protected branches.
- Make formatting, linting, type checks, tests, security-rule tests, frontend builds, and backend container builds required checks before merge or deployment.
- Separate CI from deployment jobs; deploy only from trusted protected branches or approved release tags after every required check succeeds.
- Use GitHub environments for staging and production, with branch restrictions and approval protection for production when the repository plan supports it.
- Grant the `GITHUB_TOKEN` and OIDC token only the minimum job-level permissions required; prefer OIDC workload identity over long-lived cloud credentials.
- Pin third-party actions to reviewed full-length commit SHAs and keep their source versions auditable.
- Never expose deployment secrets to workflows that execute untrusted pull-request code, and do not use `pull_request_target` to build or run untrusted changes.
- Build a versioned deployable artifact once and promote the same artifact between environments instead of rebuilding different code for production.
- Serialize deployments per environment with concurrency controls, while canceling superseded CI runs when safe.
- Make deployments traceable to a commit and environment, and keep rollback or redeployment procedures documented and testable.