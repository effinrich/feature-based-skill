# feature-based-skill

Portable feature-based-skill plus the per-project agent workflow files that point at them.

## Install a skill (global, for every project)

```
npx skills add effinrich/agent-skills --skill feature-based-architecture -g -a cursor -a claude-code -a codex -a windsurf -y
```

This installs to `~/.agents/skills/feature-based-architecture/`.

## Per-project agent files

`templates/agent-workflow/` holds `AGENTS.md`, `CLAUDE.md`, `.cursor/rules/`, and `.windsurf/rules/`. Copy them into each new project's root, then fill in the `<...>` placeholders in `AGENTS.md` and `10-project-context`. The skill is installed globally; these files are copied per project.

## Layout

```
skills/<skill>/                  SKILL.md, REFERENCE.md, scripts/
templates/agent-workflow/        AGENTS.md, CLAUDE.md, .cursor/rules/, .windsurf/rules/
```
