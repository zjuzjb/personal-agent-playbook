# Personal Agent Playbook

This repository is the source of truth for personal agent development skills,
rules, flows, templates, and project adapters.

It is intentionally separate from any product repository. Product repositories
can copy or reference the relevant pieces, but they should not host the global
playbook.

## Scope

Include:

- Personal development rules and operating defaults.
- Reusable agent workflows and skills.
- Templates for project `AGENTS.md`, handoffs, review gates, worktrees, and UI
  acceptance.
- Domain skills that are useful across multiple investment-research projects.
- Project adapters that make the core playbook fit a specific repository.

Exclude:

- System skills, plugin skills, and third-party tools.
- External tool internals.
- Non-personal or unrelated skills.
- Product-specific facts inside core rules.

## Structure

```text
rules/       Stable behavioral rules for agents.
flows/       Larger development lifecycle workflows.
skills/      Installable or copyable skill folders.
templates/   Files to seed new projects.
adapters/    Project-specific overlays.
docs/        Maintenance and portability guidance.
install/     Future install/sync helpers.
```

## Use In A New Project

1. Start with `templates/AGENTS.project.md`.
2. Add only the adapters that fit the project.
3. Copy core skills only when the project needs those workflows.
4. Keep project facts in the project adapter, not in core rules.
5. If a rule proves project-specific, move it out of core.

## Ownership Rule

Every item should have an explicit classification in `inventory.md`:

- `personal`: reusable personal method.
- `project-derived`: extracted from a project, but generalized.
- `project-adapter`: intentionally project-specific.
- `external-tool`: dependency or tool routing only; do not copy internals.
- `third-party`: not part of this playbook.
- `unknown`: exclude until ownership is confirmed.
