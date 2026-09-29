---
trigger: always_on
description: Where tests and stories go, and how to verify changes in this repo.
---

# Testing and verification

## Tests and stories

- When they exist, tests and stories sit beside the component in its folder: `focus/focus.test.tsx`, `focus/focus.stories.tsx`.
- If the repo has no test runner (see `10-project-context`), do not invent one or add test files unless asked.

## Verify every change

Exact commands are in `10-project-context`.

- Lint: 0 errors (existing warnings may stay).
- Type-check: 0 errors, for every tsconfig whose source changed.
- Feature layout: `node ~/.agents/skills/feature-based-architecture/scripts/validate.mjs` (or `.agents/skills/feature-based-architecture/scripts/validate.mjs` when vendored).
- UI changes: exercise the changed flow in the browser against the dev server. Reuse a running server; do not start a second one.
