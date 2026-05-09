---
name: project-handoff
description: Save or restore compact coding-work context for a repository. Use when switching threads, pausing work, handing off to another agent, resuming a project after restart, or preserving decisions, blockers, verification, and next steps in repo-local files.
---

# Project Handoff

Use this skill to keep project state durable without pasting long transcripts
into future conversations.

## Storage

Prefer repo-local files:

- `.ai/handoff.md` for the current compact state.
- `.ai/checkpoints/<timestamp>.md` for detailed pause points.
- `.ai/project-memory.md` for stable rules or conventions that should survive
  many sessions.

If the project already has a handoff location, use the project convention.

## Save

Record:

- Current goal.
- Summary.
- Status.
- Completed work.
- In-progress work.
- Blockers.
- Verified checks.
- Checks not run.
- Next steps.
- Important context.
- Key files.
- Commands.
- Decisions.
- Candidate memory updates.

Keep it high signal. Do not store secrets, raw logs, full transcripts, or
speculative ideas as facts.

## Resume

1. Read the latest handoff.
2. Check freshness against current git status and project state.
3. Tell the user whether it is fresh, stale, or diverged.
4. Continue from the next useful step instead of restarting from scratch.

## Freshness

- `fresh`: handoff matches current branch, key files, and known state.
- `stale`: usable but likely missing newer changes.
- `diverged`: current repo state conflicts with the handoff; inspect before
  acting.

