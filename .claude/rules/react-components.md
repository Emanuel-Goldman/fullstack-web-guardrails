---
paths:
  - "frontend/src/**/*.tsx"
---

# React Component Rule

- Use function components and hooks; follow the conventions already established by the project.
- Keep components focused on one UI responsibility and extract reusable behavior into hooks or plain functions.
- Prefer composition and explicit props over large components controlled by many boolean flags.
- Keep business and persistence logic out of presentational components.
- Use stable semantic identifiers for list keys; never use an array index when items can reorder, be inserted, or be removed.
- Make loading, empty, error, and success states explicit.
- Do not introduce memoization until a real render or computation cost justifies it.
