---
name: research-desk-product-challenger
description: Use for pre-development Research Desk product, UX, information-architecture, and investment-research workflow challenge reviews, especially major UI redesigns, research-thread/case-file design, Data Room or provenance UX, memo structure, or when the user asks for a challenger, reviewer, design critique, or another thread to debate a product plan before implementation.
---

# Research Desk Product Challenger

Use this skill to pressure-test a Research Desk product or UX proposal before
implementation. This is a requirements-design review, not a PR Risk Gate and
not an implementation workflow.

Read first:

- `AGENTS.md`
- `docs/codex/README.md`
- `docs/codex/SKILL_ROUTING.md`
- `docs/codex/MODEL_ROUTING.md`
- `docs/codex/UI_ACCEPTANCE.md` when UI is affected
- `personal-equity-research-team` for product and investment-workflow fit

## Core Rule

If the user explicitly asks for a challenger, reviewer, design critique, or
another thread to debate a product plan, the main thread may start the review.

If the main thread wants to start this review proactively, ask the user first.
Do not auto-spawn product challenger or external design reviewer threads without
user confirmation.

## Scope

Use for:

- major UI or information-architecture changes;
- research-thread, case-file, memo, Data Room, evidence, or provenance UX;
- changes to how Research Desk forms, explains, challenges, or tracks an
  investment judgment;
- product plans that risk becoming a dashboard, static report, or content pile;
- ambiguous design tradeoffs that should be clarified before opening issues or
  coding.

Do not use for:

- PR diff safety review; use `review-gate`;
- routine implementation or debugging;
- tiny copy/style fixes;
- replacing the user's final product decision.

## Workflow

1. Frame the proposal:
   - user problem and decision supported;
   - current proposal or wireframe;
   - product constraints and non-goals;
   - known concerns and open questions.
2. Choose reviewers:
   - product / investment-workflow challenger for product logic;
   - visual / interaction / information-architecture reviewer when visual
     quality and IA both matter;
   - one reviewer for narrow questions, two when product logic and visual/IA
     quality both matter;
   - default to one review round.
3. Brief reviewers narrowly. Reviewers should challenge the proposal, not
   redesign the whole product from scratch unless explicitly asked.
4. Synthesize into:
   - accepted changes;
   - rejected or deferred suggestions;
   - remaining product tradeoffs;
   - questions that genuinely need human confirmation.
5. Confirm before development. If the result implies meaningful product, UI, or
   workflow work, create or update the relevant GitHub issue through the project
   issue flow before implementation.

## Reviewer Brief Template

```text
Role: Product / UX challenger. Review only; do not implement.

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
- Better structure or wireframe if needed
- Tradeoffs requiring human confirmation
```

For visual review, add:

```text
Focus on visual hierarchy, density, spacing, responsive behavior, component
shape, modernity, and whether the UI still feels like a dashboard or report.
```

## Main-Thread Output

Return:

- conclusion and recommended direction;
- refined structure or wireframe;
- what changed because of the challenger review;
- human confirmation points;
- whether the next step is issue creation, design artifact, or implementation.
