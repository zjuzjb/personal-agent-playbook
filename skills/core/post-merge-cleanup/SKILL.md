---
name: post-merge-cleanup
description: Run checked cleanup after accepted merges. Use after PRs are merged or integrated to inspect and optionally remove local worktrees, local branches, and remote task branches without deleting uncertain work.
---

# Post-Merge Cleanup

Use this skill after one or more PRs have been merged or integrated.

## Rules

- Cleanup is checked, not fully automatic.
- Never delete dirty or uncertain work.
- Never delete the active project directory.
- Confirm branch containment before removing a branch or worktree.
- Preserve worktrees with debugging, comparison, reproduction, or follow-up
  value.
- Stop services from a worktree before deleting it.

## Workflow

1. Identify merged PRs, task branches, target branch, and issue status.
2. List local worktrees and branch containment.
3. For each candidate worktree:
   - check cleanliness;
   - check whether branch is contained in the target branch;
   - check whether it is active or still useful;
   - check whether any service is running from it.
4. Remove only safe worktrees and merged task branches.
5. Delete remote task branches only when the PR is merged and the branch is not
   intentionally preserved.
6. Report preserved items with reasons.

## Output

Return:

- Removed worktrees.
- Removed local branches.
- Removed remote branches.
- Preserved worktrees or branches and why.
- Running services stopped.
- Follow-up cleanup that needs human decision.

