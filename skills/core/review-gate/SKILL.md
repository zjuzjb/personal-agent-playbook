---
name: review-gate
description: Apply Completion Gate and Risk Gate rules for PRs or completed task branches. Use when a PR is ready for review, when deciding whether to start a reviewer, or when preparing a human acceptance guide.
---

# Review Gate

Use this skill to decide whether work is complete, whether a separate reviewer
is needed, and what the human should inspect.

## Inputs

- Linked issue, PR, branch, or task.
- Target branch.
- Acceptance criteria.
- Changed files.
- Verification evidence.
- Known risks or non-goals.

## Workflow

1. Run Completion Gate as the main thread:
   - requested outcome met;
   - scope and non-goals respected;
   - primary user path checked;
   - verification evidence present.
2. Classify risk:
   - low: small diff, local behavior, strong verification;
   - medium: multiple files, local API/state/workflow change, meaningful UI;
   - high: data, finance, security, auth, migrations, production config, broad
     refactor, architecture, or investment conclusions.
3. Decide reviewer gate:
   - low risk: reviewer can be skipped with a recorded reason;
   - medium risk: reviewer recommended by default;
   - high risk: reviewer mandatory before human final approval.
4. If reviewer is needed, prepare a narrow reviewer brief.
5. Prepare a concrete human acceptance guide.

## Reviewer Brief

```text
Role: Reviewer / QA only. Do not expand scope or make large changes.

Issue / PR:
Goal:
Non-goals:
Base branch:
Head branch:
Risk level and rationale:
Completion Gate evidence already checked:
Files / modules to inspect:
Required verification commands or screenshots:
Specific risk questions:
Expected output:
- Verdict: mergeable / needs changes / needs human focus
- Main issues, if any
- Commands run and results
- Diff boundary assessment
- Human focus areas
```

## Output

Return:

- Done state.
- Completion Gate result.
- Risk level and reasons.
- Reviewer gate: skipped / recommended / mandatory.
- Reviewer brief if needed.
- Human acceptance guide.
- Verification commands and results.
- Remaining risks or follow-ups.

