# Main Thread And Subthread Flow

Use this when work benefits from specialist isolation.

## Main Thread Owns

- Product direction.
- Acceptance criteria.
- Task decomposition.
- Risk and model routing.
- Worktree and branch assignment.
- Final integration.
- Completion Gate.
- Human acceptance handoff.

## Subthread Owns

- Bounded specialist implementation or analysis.
- Files and modules explicitly assigned to it.
- Local validation in its own worktree.
- Concise handoff.

## Split Only When

- The work is recurring or specialist-heavy.
- Context noise would pollute the main thread.
- The task can be isolated with clear ownership.
- The output can be independently verified.

Do not split tiny local edits just to use parallelism.

