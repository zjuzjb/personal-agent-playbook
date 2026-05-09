# Research Desk Rules

These are adapter rules, not global rules.

## Product

- Research Desk is web-only.
- It is a private AI investment research team for individual investors.
- It is not a generic dashboard or automatic report generator.
- User-facing research must provide:
  - current opinion;
  - why;
  - what would change the judgment;
  - what the team will watch next.

## Data

- Every key number needs source, date, formula, period, unit, and provenance.
- Do not invent data, estimates, valuation assumptions, sources, or runtime
  records.
- Missing data must be routed as fetchable, computable, provider-required, or
  user-required.

## Delivery

- Meaningful development should trace to a PRD, epic, GitHub issue, or explicit
  quick fix.
- Completed implementation work should produce a PR unless the task is
  explicitly local-only.
- Do not merge before Human Accepted status.

## Main Thread

The main thread owns product direction, investment-research logic, architecture
boundaries, task splitting, model routing, final acceptance, merge decisions, and
handoff state.

Execution-heavy implementation should usually be delegated to bounded
subthreads with independent worktrees and branches.

