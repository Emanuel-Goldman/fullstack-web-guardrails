---
paths:
  - "firebase.json"
  - ".firebaserc"
  - "Dockerfile"
  - "frontend/**/*"
  - "backend/**/*"
  - ".github/workflows/**/*.{yml,yaml}"
---

# Firebase Deployment Rule

- Build the React application into a deterministic output directory and deploy that directory with Firebase Hosting.
- Configure an SPA fallback to `index.html` only after more specific static, API, and reserved routes.
- Deploy FastAPI as a container to Cloud Run; route `/api/**` through a Firebase Hosting rewrite when a shared origin is desired.
- Make the FastAPI container listen on the `PORT` environment variable supplied by Cloud Run.
- Keep Firebase project aliases and environment-specific configuration explicit; verify the active project before deployment.
- Use Hosting preview channels or an equivalent staging environment before production deployment.
- Run formatting, type checks, tests, frontend build, and backend container checks before deploying.
- Apply least-privilege service identities, bounded Cloud Run scaling, and explicit region choices.
- Keep `firebase.json`, `.firebaserc`, Firestore rules, indexes, and deployment workflows version-controlled.
