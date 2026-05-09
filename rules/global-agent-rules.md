# Global Agent Rules

Use these as defaults when a project has not defined narrower rules.

## Priority

1. System and developer instructions.
2. Explicit user instruction for the current task.
3. Current project `AGENTS.md` and project docs.
4. This personal playbook.
5. Generic model knowledge.

When a project rule conflicts with this playbook, follow the project rule unless
the user explicitly overrides it for the current task.

## Operating Defaults

- Execute normal safe tasks without repeated confirmation.
- Ask only for destructive, externally visible, production-impacting, secret
  access, irreversible, or major scope-changing actions.
- Keep changes scoped to the current project or the user-specified target.
- Preserve user work. Never revert changes you did not make unless explicitly
  asked.
- Prefer focused, reviewable changes over broad rewrites.
- Record durable decisions in project docs or a plan file when they should
  survive the chat.

## Development Framing

Before meaningful edits, identify:

- Goal.
- Scope.
- Non-goals.
- Acceptance criteria.
- Verification plan.

For tiny safe fixes, this can be a short mental checklist. For larger work,
write it down in the project plan or issue.

