---
name: requirements-red-team-review
description: Red-team product requirements, PRDs, issue briefs, UX or information-architecture proposals, acceptance criteria, and implementation plans before development. Use when the user asks for 需求分析红方 review, requirement critique, product challenger, red-team review, PRD review, spec review, plan challenge, scope risk review, or asks whether a requirement is clear enough to build.
---

# Requirements Red-Team Review

Use this skill before implementation when the expensive failure would be
building the wrong thing. This is a requirements-design review, not a PR Risk
Gate and not an implementation workflow.

The goal is not to make the requirement bigger. The goal is to expose ambiguity,
contradiction, missing user value, hidden scope, weak acceptance criteria, and
unverifiable claims early.

## Inputs

- User request, PRD, issue, epic, or plan.
- Target user and use case.
- Current product constraints.
- Proposed scope and non-goals.
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

If the user explicitly asks for a challenger or another thread to debate a
product plan, the main thread may start the review. If the main thread wants to
start this proactively, ask the user first.

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

## Reviewer Brief

```text
Role: Product / requirements challenger. Review only; do not implement.

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
- Better structure or flow if needed
- Tradeoffs requiring human confirmation
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
