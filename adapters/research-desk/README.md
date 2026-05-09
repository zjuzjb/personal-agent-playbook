# Research Desk Adapter

This adapter captures Research Desk-specific rules that should not become
global defaults.

Use it only for Research Desk or a directly similar product.

## Applies When

- The project is a web-only personal investment research product.
- GitHub issues drive meaningful development work.
- The project uses explicit done states and human acceptance before merge.
- Research outputs need provenance, current opinion, change conditions, and
  watch items.

## Do Not Generalize

Keep these adapter-only:

- Research Desk product identity.
- Research Desk tab names and information architecture.
- Project-specific GitHub labels and issue lifecycle.
- Integration branch names.
- Local preview scripts and ports.
- Repo paths and environment assumptions.

## Core Dependencies

Use these playbook items:

- `skills/core/review-gate`
- `skills/core/post-merge-cleanup`
- `skills/core/specialist-subthread`
- `skills/domain/personal-equity-research-team`
- `skills/domain/research-qa-auditor`
- `skills/domain/sec-xbrl-data-engineer`

