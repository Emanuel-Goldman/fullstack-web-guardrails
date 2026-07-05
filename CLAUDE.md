# Repository Guidance

## Purpose

This repository provides reusable Claude Code rules for building clear, tested full-stack web applications with React, TypeScript, FastAPI, Python, Firebase Hosting, and Cloud Firestore.

## Repository layout

- `.claude/rules/` contains modular, path-scoped rules.
- `CLAUDE-RULES.md` contains the complete rule set in one copy-paste-ready file.
- `README.md` explains adoption, stack choices, and contribution expectations.
- `LICENSE` contains the MIT license.

## Working in this repository

- Treat every rule as user-facing documentation.
- Keep instructions direct, observable, and specific enough to affect an implementation decision.
- Keep one coherent concern per modular rule file.
- Preserve YAML frontmatter and use repository-relative glob patterns.
- Keep `CLAUDE-RULES.md` semantically synchronized with every modular rule.
- Do not weaken security, validation, test, or deployment safeguards for convenience.
- Prefer official React, TypeScript, FastAPI, Python, Firebase, and Google Cloud terminology.

## Validation checklist

1. Confirm every modular rule has valid frontmatter and an intentional path scope.
2. Check that rules do not conflict or repeat the same guidance unnecessarily.
3. Verify that `CLAUDE-RULES.md` contains every modular rule bullet.
4. Update the README table whenever a rule is added, removed, or renamed.
5. Run Markdown and whitespace checks before committing.
