---
paths:
  - "frontend/src/**/*.{ts,tsx}"
---

# React State and Effects Rule

- Store the minimum state needed; derive values during rendering when they can be calculated from props or existing state.
- Keep state close to the components that own it and lift it only when multiple consumers truly need the same source of truth.
- Use Effects to synchronize with external systems, not to reproduce ordinary data flow.
- Declare complete Effect dependencies and restructure unstable logic instead of disabling dependency lint rules.
- Clean up subscriptions, listeners, timers, and in-flight work when an Effect is replaced or a component unmounts.
- Prevent stale responses from overwriting newer state when requests can race.
- Use a consistent data-fetching layer rather than scattering raw fetch and Firestore calls through components.
