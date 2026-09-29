# Agent instructions

Canonical instructions for any agent.

> **Architecture skill, required:** follow the feature-based-architecture skill for new projects and for structural refactors (creating, moving, or splitting a component or feature file, or extracting types/consts/hooks/helpers). It is installed for the user at `~/.agents/skills/feature-based-architecture/SKILL.md`. When this repo vendors the skill, use the project copy at `.agents/skills/feature-based-architecture/SKILL.md`.

`.cursor/rules/*.mdc` and `.windsurf/rules/*.md` carry the same rules for tools that do not load this file (`00-core-principles`, `10-project-context`, `20-frontend`, `30-testing`). Change a rule here and in both rule folders in the same edit. A rule that belongs in the skill itself changes in the skill's source repo too.

## React structure (`src/`)

- One React component per file, named after the component in kebab-case: `TaskCard` -> `task-card.tsx`. Each component or screen lives in a like-named folder (`task-list/task-list.tsx`); partials stay flat in `partials/`. Lint enforces one-per-file and kebab-case as errors (`react/no-multi-comp`, `unicorn/filename-case`).
- Keep files under ~200 lines. Refactors move code without changing behavior, and are incremental: bring the files you touch into line; leave untouched files where they are.
- Existing app-level folders stay where they are; new cross-feature code goes in `src/shared/{ui,hooks,types,consts,utils}` per the skill.
- Verify with the commands listed in `10-project-context` and `30-testing`.
- When code moves or is renamed, update every doc that names the old path (`README.md`, handoff or plan notes, this file, the rule folders, the skill) in the same change.
- Do not commit or push unless asked.

## Learned User Preferences

- Prioritize small, readable files: component files are markup plus wiring; types, consts, hooks, and helpers go in sibling files.
- Sibling files beside a component are unprefixed (`types.ts`, `consts.ts`, `hooks.ts`, `utils.ts`), never `task-list.types.ts`.
- Name a screen's folder and file after its feature (`focus/focus.tsx`), not a descriptive variant like `focus-radar-modal`.

## Learned Workspace Facts

- `AGENTS.md` is the canonical agent instruction file; `CLAUDE.md` only imports it with `@AGENTS.md`. `.cursor/rules/` and `.windsurf/rules/` mirror it for Cursor and Windsurf.
- <Data layer, e.g. "Postgres via Drizzle", and any data layers to ignore guidance for.>
- <Backend entry and routing, e.g. "`server.ts` plus one router per endpoint in `routes/`".>
- <Reference component folder, e.g. "`src/features/<feature>/<component>/` is the worked example of the layout".>
