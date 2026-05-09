# Research Desk Issue Flow

Use this adapter when the user asks to process the next ready Research Desk
issue.

## Pick Issue

- Select open issues with `status:ready`.
- Skip `status:blocked`.
- Sort by priority: `priority:P0`, then `priority:P1`, `priority:P2`,
  `priority:P3`.
- Process only one issue at a time.
- If the issue is incomplete, comment for clarification and stop.

## Task Card

Produce:

- Issue number.
- Goal.
- Scope.
- Non-goals.
- Acceptance criteria.
- Risk level.
- Reviewer gate decision.
- Expected done state.
- Skill routing decision.
- Worktree and branch plan.
- Implementation path.

## Branch / Worktree

- Branch pattern: `codex/issue-{issue_number}-{short-title}`.
- Use an independent worktree for development beyond quick fixes or docs-only
  edits.
- Do not work directly on `main`.
- If current worktree is dirty with unrelated changes, create a clean sibling
  worktree from the intended base.

## Validate

- Run relevant tests and build checks.
- For UI, include browser or screenshot validation when possible.
- For data logic, include sample validation, edge cases, and regression checks.

## PR And Issue Update

PR description should include:

- linked issue;
- done state;
- target branch;
- risk level and rationale;
- reviewer gate decision and verdict if run;
- changes;
- files touched;
- tests and QA;
- screenshots if UI changed;
- data validation if data changed;
- remaining risks;
- human acceptance guide.

After PR creation:

- move issue from `status:ready` to `status:review`;
- remove `status:in-progress` if present;
- comment with PR link, state, summary, verification, risk, target branch, and
  acceptance guide;
- stop and wait for human review.

