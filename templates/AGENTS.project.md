# Project Agent Instructions

Project rules override the personal playbook when they conflict.

## Startup

- Read this file before starting tasks.
- Read project-specific docs referenced below.
- Preserve user work.
- Do not make broad product, architecture, UI, data, or workflow changes without
  a plan.
- After changes, run relevant checks or state exactly why they could not be run.

## Task Framing

Before meaningful edits, identify:

- Goal.
- Scope.
- Non-goals.
- Acceptance criteria.
- Verification plan.

## Hard Rules

- Keep changes small and reviewable.
- Avoid unrelated refactors.
- Do not change public API behavior unless explicitly requested.
- Do not introduce new production dependencies without explaining why.
- Do not delete files, wipe data, force-push, or change production config without
  explicit approval.

## Verification

Run checks that match the changed surface:

- lint
- typecheck
- tests
- build
- UI QA
- data validation

Report exact commands and results.

## Output Format

For development or documentation-change wrap-ups, use:

- Summary
- Files changed
- Verification
- Risks / follow-ups

