---
paths:
  - "frontend/**/*.{ts,tsx,json}"
  - "backend/**/*.{py,toml,txt}"
---

# Performance and Dependencies Rule

- Measure a real bottleneck before making performance-driven changes.
- Avoid unnecessary React renders, repeated network requests, unbounded Firestore listeners, and repeated expensive transformations.
- Paginate large results and load code or data incrementally when it materially improves user experience.
- Keep the frontend bundle intentional; prefer platform features and existing dependencies over adding a package for trivial behavior.
- Add dependencies only when their maintenance, security, bundle, and operational costs are justified.
- Pin or lock dependency versions through the project's package and Python dependency tooling.
- Do not perform blocking I/O in FastAPI async routes.
- Set explicit timeouts and resource limits for external calls and deployed services.
- Preserve readability unless measurement shows that a less obvious optimization is necessary.
