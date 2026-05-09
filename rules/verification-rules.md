# Verification Rules

Run checks that match the risk and changed surface.

## Defaults

- Docs-only: `git diff --check`.
- TypeScript / web app: lint, typecheck if available, tests, and build.
- UI: browser QA, screenshots for affected viewports, and responsive checks.
- Data logic: deterministic tests for sources, formulas, periods, units, and
  provenance.
- Scripts: direct command execution with success and failure cases where cheap.

## Reporting

Always report:

- Exact commands run.
- Pass/fail result.
- Checks not run and why.
- Residual risk.

Do not claim completion solely from code edits. User-facing workflows need a real
path check whenever feasible.

