---
name: research-desk-product-challenger
description: Use for pre-development Research Desk product, UX, information-architecture, and investment-research workflow challenge reviews, especially major UI redesigns, research-thread/case-file design, Data Room or provenance UX, memo structure, or when the user asks for a challenger, reviewer, design critique, or another thread to debate a product plan before implementation.
---

# Research Desk Product Challenger

Use this Research Desk adapter with the core `product-challenger` skill to
pressure-test a product or UX proposal before implementation. This is a
requirements-design review, not a PR Risk Gate and not an implementation
workflow.

Read first:

- `AGENTS.md`
- `docs/codex/README.md`
- `docs/codex/SKILL_ROUTING.md`
- `docs/codex/MODEL_ROUTING.md`
- `docs/codex/UI_ACCEPTANCE.md` when UI is affected
- `product-challenger` for the portable challenger workflow
- `personal-equity-research-team` for product and investment-workflow fit

## Core Rule

Follow the core `product-challenger` trigger rule. This adapter adds Research
Desk-specific product and investment-research checks.

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

## Research Desk Extra Checks

In addition to the core challenger lenses, check:

- Does this help the investor make or revise a judgment, or is it only a nicer
  container for content?
- Does it preserve source, date, formula, period, unit, and provenance for key
  numbers?
- Does it show current opinion, why, what would change it, and what the team
  will watch next?
- Does it avoid becoming a generic dashboard, static sell-side report, or dense
  content pile?
- Does the flow fit a continuous research case file instead of a one-shot
  generated report?
- If implementation is needed, should it create or update a GitHub issue before
  coding?

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
