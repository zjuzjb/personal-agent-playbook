---
name: product-challenger
description: Challenge product requirements, PRDs, issue briefs, UX or information-architecture proposals, acceptance criteria, and implementation plans before development. Use when the user asks for 需求分析红方 review, product challenger, requirement critique, red-team review, PRD review, spec review, design critique, plan challenge, scope risk review, or asks whether a requirement is clear enough to build.
---

# Product Challenger

Use this skill before implementation when the expensive failure would be
building the wrong thing. This is a requirements-design review, not a PR Risk
Gate and not an implementation workflow.

The goal is not to make the requirement bigger. The goal is to expose ambiguity,
contradiction, missing user value, hidden scope, weak acceptance criteria, and
unverifiable claims early.

## Core Rule

If the user explicitly asks for a challenger, red-team review, design critique,
or another thread to debate a product plan, the main thread may start the
review.

If the main thread wants to start this review proactively, ask the user first.
Do not auto-spawn product challenger or external reviewer threads without user
confirmation.

## Inputs

- User request, PRD, issue, epic, or plan.
- Target user and use case.
- Current product constraints.
- Proposed scope and non-goals.
- Current proposal, wireframe, or flow if UI/IA is affected.
- Known concerns and open questions.
- Acceptance criteria.
- Verification plan.

If an input is missing, infer the smallest useful assumption and mark it as an
assumption instead of stopping unless the missing item makes review impossible.

## Scope

Use for:

- major product, UX, or information-architecture changes;
- changes to how a product forms, explains, challenges, or tracks a user
  judgment;
- plans that risk becoming a dashboard, static report, content pile, or polished
  but low-value feature;
- ambiguous tradeoffs that should be clarified before opening issues or coding.

Do not use for:

- PR diff safety review; use a review-gate skill instead;
- routine implementation or debugging;
- tiny copy or style fixes;
- replacing the user's final product decision.

## Review Lenses

1. User problem:
   - Is the real user problem explicit?
   - Is the current workaround or pain clear?
   - Does the proposed work reduce effort, risk, or uncertainty?
2. Scope:
   - What is included?
   - What is explicitly not included?
   - What hidden work is implied?
   - Is the smallest useful slice defined?
3. Acceptance:
   - Can a reviewer decide pass/fail without guessing?
   - Are edge cases and failure states covered?
   - Is there a concrete manual or automated verification path?
4. Product risk:
   - Could this create a polished but low-value feature?
   - Does it conflict with product positioning or workflow?
   - Does it add maintenance cost without durable value?
5. Technical risk:
   - Are data, state, API, security, performance, or migration assumptions
     hidden?
   - Is implementation ownership clear?
   - Are dependencies and integration points explicit?
6. Sequencing:
   - What must be decided before coding?
   - What can be deferred?
   - What should become a follow-up issue instead of current scope?

## Workflow

1. Frame the proposal:
   - user problem and decision supported;
   - current proposal or wireframe;
   - constraints and non-goals;
   - known concerns and open questions.
2. Choose review depth:
   - one challenger for narrow requirement or scope questions;
   - product plus visual/IA reviewers only when both product logic and interface
     quality materially matter;
   - default to one review round.
3. Brief reviewers narrowly. Reviewers should challenge the proposal, not
   redesign the whole product from scratch unless explicitly asked.
4. Synthesize:
   - accepted changes;
   - rejected or deferred suggestions;
   - remaining product tradeoffs;
   - questions that genuinely need human confirmation.
5. Confirm before development. If the result implies meaningful product, UI, or
   workflow work, update the issue, PRD, or plan before implementation.

## Reviewer Brief

```text
Role: Product / UX / requirements challenger. Review only; do not implement.

Project goal:
User decision supported:
Current proposal:
Constraints:
Non-goals:
Known concerns:
Specific questions:
Expected output:
- Verdict: pass / conditional pass / fail
- 5-8 strongest challenges
- Better structure, flow, or wireframe if needed
- Tradeoffs requiring human confirmation
```

For visual or IA review, add:

```text
Focus on visual hierarchy, density, spacing, responsive behavior, component
shape, modernity, and whether the UI supports the user's decision instead of
becoming a generic dashboard or content pile.
```

## Output

Return findings first, ordered by severity:

- Blocking ambiguity.
- Scope or product mismatch.
- Missing acceptance criteria.
- Hidden technical risk.
- Suggested rewrite.
- Minimum buildable slice.
- Verification plan.

Use direct language. Do not bury blockers under encouragement.

The main thread should synthesize challenger output instead of dumping raw
reviewer text. Convert it into accepted changes, rejected or deferred
suggestions, remaining tradeoffs, and questions that genuinely need human
confirmation.

## Suggested Rewrite Format

```markdown
## Goal

## Scope

## Non-goals

## Acceptance Criteria

## Verification

## Open Questions
```

## Pass Condition

A requirement is ready for implementation only when:

- the user problem is clear;
- scope and non-goals are explicit;
- acceptance criteria are testable;
- the smallest useful slice is identified;
- unresolved questions are either answered or explicitly deferred;
- verification is realistic for the project.
