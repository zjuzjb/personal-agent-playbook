---
name: specialist-subthread
description: Standardize when and how to split recurring, context-heavy, specialist development work into a dedicated subthread or delegated agent. Use when the user asks to create a subthread, keep the main thread clean, hand work to a data/security/performance/QA/design/agent specialist, or make a reusable multi-thread development workflow.
---

# Specialist Subthread

Use this skill to turn an ad-hoc "let another thread handle it" idea into a
repeatable workflow with clear ownership, inputs, outputs, and reintegration.

## Core Rule

Do not split work merely because it is large. Split when the work is:

- recurring across the project or future projects;
- context-heavy enough to pollute the main thread;
- specialist enough to need its own quality gates;
- likely to produce reusable docs, tests, modules, or operational habits.

If the task is small and safe to finish locally, do it locally.

## Workflow

1. Classify the specialty: data reliability, security, performance, QA
   automation, design system, release engineering, or agent orchestration.
2. Define the boundary:
   - Main thread owns product goal, acceptance, final tradeoffs, and user-facing
     decisions.
   - Subthread owns specialist implementation, validation, reusable assets, and
     risk report.
3. Write a brief with role, mission, context, scope, non-goals, inputs,
   constraints, plan, validation, deliverables, and return format.
4. Choose execution mode:
   - If the user explicitly asks for delegated agent work, spawn the worker with
     the brief.
   - Otherwise provide the brief for a separate thread.
   - If the next local step is blocked by the result, do the blocking work
     locally.
5. Reintegrate:
   - Review returned changes or report.
   - Verify against acceptance criteria.
   - Run relevant checks.
   - Decide whether this specialty split should become a project default.

## Brief Template

```markdown
# Specialist Subthread Brief

## Role
You are the [specialty] specialist for this project.

## Mission
[One sentence describing the outcome.]

## Context
- Project: [name/path]
- Current product goal: [goal]
- Why this belongs in a specialist subthread: [reason]

## Scope
- [Concrete task]

## Non-goals
- [What not to change]
- [What decisions remain in the main thread]

## Inputs
- [Relevant files/docs/config]
- [Known decisions]

## Constraints
- Preserve unrelated user changes.
- Keep edits scoped to owned files/modules.
- Prefer deterministic logic and tests over prompt-only fixes.
- Do not introduce destructive actions.

## Implementation Plan
- [Step]

## Validation
- [Commands]
- [Manual checks]
- [Specialist quality gates]

## Deliverables
- Code/docs/tests changed.
- Short explanation of the chosen approach.
- Evidence that validation passed.
- Remaining risks or follow-up tasks.

## Return Format
- What changed
- Why this is correct
- How it was verified
- Remaining risk
```

## Specialist Defaults

Data reliability owns sources, correctness, extraction, calculations,
provenance, caching, incremental refresh, future-function prevention, and tests.

Security owns trust boundaries, input validation, authorization, SSRF, secrets,
supply chain, and threat modeling.

Performance owns startup, render speed, query latency, caching, bundle size, and
benchmark methodology.

QA automation owns regression scenarios, test data, browser automation, and
acceptance checklists.

Design system owns visual consistency, typography, layout rules, component
primitives, interaction states, and UI polish.

Agent orchestration owns role design, task routing, queues, retry policy, cost
control, observability, and handoff artifacts.

