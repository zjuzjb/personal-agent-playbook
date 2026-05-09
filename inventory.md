# Inventory

This inventory records what was considered, where it belongs, and why.

## Inclusion Policy

Only `personal`, `project-derived`, and deliberate `project-adapter` material is
included. `external-tool`, `third-party`, and `unknown` material is excluded
unless ownership is later confirmed.

## Core Includes

| Source | Ownership | Decision | Target | Notes |
|---|---:|---:|---|---|
| `~/.codex/skills/specialist-subthread` | personal | include | `skills/core/specialist-subthread` | Main-thread / specialist-thread split method. |
| `~/.codex/skills/plan-todo-manager` | personal | include | `skills/core/plan-todo-manager` | Living plan and backlog discipline. |
| `~/.codex/skills/project-handoff` | personal | adapt | `skills/core/project-handoff` | Kept as a portable handoff contract; local scripts are not copied in v1. |
| Generalized product challenger / requirements red-team method | personal | include | `skills/core/product-challenger` | Portable challenger review for PRDs, issue briefs, UX/IA plans, scope, acceptance, and verification before coding. |
| Research Desk `.agents/skills/review-gate` and `docs/codex/REVIEW_GATE.md` | project-derived | adapt | `skills/core/review-gate`, `templates/REVIEW_GATE.md` | Generalized Completion Gate / Risk Gate / Human Acceptance pattern. |
| Research Desk `.agents/skills/post-merge-cleanup` and `docs/codex/WORKTREE_FLOW.md` | project-derived | adapt | `skills/core/post-merge-cleanup`, `templates/WORKTREE_FLOW.md` | Generalized checked cleanup. |
| Research Desk `docs/codex/DEV_RULES.md` | project-derived | adapt | `rules/`, `flows/`, `templates/AGENTS.project.md` | General task framing, scope, verification, and handoff rules. |
| Research Desk `docs/codex/MODEL_ROUTING.md` | project-derived | adapt | `rules/model-routing-rules.md` | General risk-based model routing. |
| Research Desk `docs/codex/UI_ACCEPTANCE.md` | project-derived | adapt | `templates/UI_ACCEPTANCE.md` | General UI acceptance, with product specifics removed. |

## Domain Includes

| Source | Ownership | Decision | Target | Notes |
|---|---:|---:|---|---|
| `~/.codex/skills/personal-equity-research-team` | personal | include | `skills/domain/personal-equity-research-team` | Product baseline for personal investment research products. |
| `~/.codex/skills/sec-xbrl-data-engineer` | personal | include | `skills/domain/sec-xbrl-data-engineer` | SEC/XBRL data reliability method. |
| `~/.codex/skills/research-qa-auditor` | personal | include | `skills/domain/research-qa-auditor` | Equity research output QA gate. |
| `~/.codex/skills/social-research-signal-extractor` | personal | include | `skills/domain/social-research-signal-extractor` | Grounded signal extraction from authorized text. |
| `~/.codex/skills/thesis-tracker` | personal | include | `skills/domain/thesis-tracker` | Falsifiable thesis tracking. |
| `~/.codex/skills/catalyst-calendar` | personal | include | `skills/domain/catalyst-calendar` | Catalyst tracking objects. |
| `~/.codex/skills/earnings-preview` | personal | include | `skills/domain/earnings-preview` | Pre-earnings setup and follow-up framework. |

## Project Adapter Includes

| Source | Ownership | Decision | Target | Notes |
|---|---:|---:|---|---|
| Research Desk `AGENTS.md` and `docs/codex/*` | project-adapter | adapt | `adapters/research-desk` | Keeps Research Desk facts out of core. |
| Research Desk `.agents/skills/research-desk-issue-flow` | project-adapter | adapt | `adapters/research-desk/issue-flow.md` | Specific GitHub label/status workflow. |
| Research Desk `.agents/skills/research-desk-product-challenger` from worktree `2ec4` | project-adapter | adapt | `adapters/research-desk/skills/research-desk-product-challenger` | Research Desk-specific adapter on top of core `product-challenger`. |

## Reference Candidates

These may be personal or useful, but are intentionally not copied into core v1.
Normalize later only if the user confirms ownership and recurring use.

| Source | Ownership | Decision | Notes |
|---|---:|---:|---|
| `~/.codex/skills/3-statement-model` | personal-or-unknown | reference | Institutional method library candidate. |
| `~/.codex/skills/comps-analysis` | personal-or-unknown | reference | Institutional method library candidate. |
| `~/.codex/skills/dcf-model` | personal-or-unknown | reference | Institutional method library candidate. |
| `~/.codex/skills/initiating-coverage` | personal-or-unknown | reference | Institutional method library candidate. |
| `~/.codex/skills/earnings-analysis` | personal-or-unknown | reference | Current format is institutional report-oriented. |
| `~/.codex/skills/competitive-analysis` | personal-or-unknown | reference | Useful method, not a default development skill. |
| `~/.codex/skills/model-update` | personal-or-unknown | reference | Legacy reference candidate. |
| `~/.codex/skills/morning-note` | personal-or-unknown | reference | Legacy reference candidate. |
| `~/.codex/skills/idea-generation` | personal-or-unknown | reference | Legacy reference candidate. |
| `~/.codex/skills/sector-overview` | personal-or-unknown | reference | Legacy reference candidate. |

## Explicit Excludes

| Source | Ownership | Decision | Reason |
|---|---:|---:|---|
| `~/.codex/skills/gstack` and related gstack skills | external-tool | exclude | External tool internals are not personal playbook content. Only routing rules may mention external tools. |
| `~/.codex/skills/hatch-pet` | third-party-or-unrelated | exclude | Not part of the personal development method set. |
| System skills under `.system` | third-party | exclude | Use as tools, do not copy. |
| Plugin-provided skills | third-party | exclude | Use as tools, do not copy. |
| `~/.codex/skills/ccpm` | external-or-unknown | exclude | Useful dependency pattern, but not copied until ownership is clear. |
