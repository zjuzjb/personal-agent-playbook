# Project Override Rules

Project rules are adapters, not global truth.

## Source Of Truth

A project should keep its own:

- `AGENTS.md` startup rules.
- Review and merge gates.
- Branch and worktree conventions.
- Product-specific constraints.
- Verification commands.
- Domain-specific acceptance criteria.

The personal playbook supplies defaults and templates only.

## Adapter Boundary

Keep these out of core rules:

- Project name and paths.
- Product identity and positioning.
- Issue labels and status names.
- Preview scripts and ports.
- Protected branch names.
- Project-specific UI tabs or research objects.
- Repo-specific commands.

Put them in `adapters/<project-name>/` or the target project itself.

