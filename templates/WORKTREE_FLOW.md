# Worktree Flow Template

## Core Rule

Each development subthread should use:

- One independent worktree.
- One independent branch.
- One bounded task scope.

Subthreads must not edit the main thread worktree or another subthread's
worktree.

## Branch Pattern

```bash
git fetch origin
git worktree add ../<project>-<task> -b codex/<task-name> <base-branch>
cd ../<project>-<task>
```

## Main Thread Responsibilities

- Decompose tasks.
- Assign risk and model.
- Assign worktree and branch.
- Define acceptance criteria.
- Run final integration checks.
- Resolve conflicts.
- Decide merge readiness.

## Cleanup

Cleanup is checked, not automatic. Before deleting a worktree or branch, verify:

- No uncommitted or untracked user work should be kept.
- Branch commits are contained in the target branch.
- Worktree is not the active project directory.
- Worktree is not useful for debugging, comparison, or follow-up.
- Any running service is stopped or no longer needed.

