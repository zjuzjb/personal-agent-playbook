# Extraction Criteria

Use these rules when deciding whether material belongs in this playbook.

## Include

- Reusable personal methods.
- Repeated project-derived workflows after project facts are removed.
- Templates that can be filled for a new project.
- Domain methods likely to recur in future projects.

## Adapt

Adapt instead of copying when the source contains:

- Project names or paths.
- Project-specific branches, labels, ports, or scripts.
- Product positioning.
- Tool-specific commands that are not universal.

## Exclude

Exclude by default:

- System or plugin skills.
- External tool internals.
- Third-party skills.
- Unknown ownership.
- One-off project facts.
- Content that would make a new project behave like the old project by mistake.

## Promote Later

Move an item from reference to core only after it proves:

- It recurs across projects.
- It has clear trigger conditions.
- It has non-goals.
- It produces verifiable output.
- It does not require hidden project context.

