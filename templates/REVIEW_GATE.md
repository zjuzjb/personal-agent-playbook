# Review Gate Template

## Done States

- Implemented: changes exist in a task branch or worktree.
- Completion Accepted: the main thread verified the requested outcome.
- Risk Reviewed: reviewer passed or was skipped with a recorded low-risk reason.
- Human Accepted: user explicitly accepted the result.
- Integrated: merged into an integration branch.
- Landed: merged into the final base branch.
- Released: deployed or available in the intended runtime.

## Completion Gate

Owner: main thread.

Question: did we build the requested thing?

Check:

- Acceptance criteria are satisfied.
- Scope and non-goals were respected.
- Primary user path works.
- UI, workflow, and product behavior match the intent when relevant.
- Subthread handoff did not omit required work.
- Verification evidence is sufficient.

## Risk Gate

Owner: reviewer when required.

Question: is this safe, bounded, and mergeable?

Check:

- Diff stays within task boundary.
- No likely regression or hidden behavior change.
- Verification matches risk.
- Data, provenance, security, migrations, and production config are handled.
- Human focus areas are identified.

Verdict:

- `mergeable`
- `needs changes`
- `needs human focus`

## Human Acceptance Guide

Include:

- PR, preview, branch, command, or file section.
- Exact page, state, viewport, ticker, tab, or workflow when relevant.
- What changed.
- Pass criteria.
- Fail criteria.
- What does not need to be inspected.

