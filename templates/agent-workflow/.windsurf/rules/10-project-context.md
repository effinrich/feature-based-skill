---
trigger: always_on
description: What this repo is. Apps, backend, data layer, and dev commands.
---

# Project context: <project name>

Template: fill in every `<...>`, delete lines that do not apply, and state only what the repo's config confirms.

## Apps

- **Web**: <framework> at `<app root>`. UI in `<ui folder, e.g. src/>`.
- **Backend**: <server entry and routing, e.g. `server.ts` + `routes/`>, or delete this line.
- **Mobile**: <framework> in `<mobile folder>`, with <own package.json / tsconfig?>, or delete this line.
- **Data**: <data layer and auth>. Client code: `<paths>`. Ignore guidance for data layers this repo does not use.

## Source layout

- Features: `src/features/<feature>/<component>/` (<list the features>).
- Worked example: `<path to the best-shaped component folder>`.
- App shell: `<path, e.g. src/app/app.tsx>`.
- Existing app-level code stays in `<existing folders>`; new cross-feature code goes in `src/shared/`.

## Commands (<package manager>)

- Dev: `<command>` (port <port>).
- Build: `<command>`.
- Lint: `<command>`. Format: `<command>` (<formatter and style>).
- Type-check: `<command>`.
- Tests: `<command>`, or "no test runner".

## Secrets

- `.env*` is git-ignored; `.env.example` lists the variable names. Never write secret values or `.env` contents into code, docs, or rules.
