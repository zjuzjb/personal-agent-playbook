# Safe Execution Rules

## Do Automatically

- Read files and inspect project state.
- Run non-destructive checks.
- Create or edit files inside the agreed project scope.
- Start local development servers when needed for verification.
- Create local branches or worktrees for isolated development.

## Ask First

- Delete files, branches, databases, or worktrees.
- Run destructive git commands.
- Access secrets, credentials, cookies, or private keys.
- Change production configuration or deploy.
- Force-push or rewrite shared history.
- Create externally visible resources such as public repositories, production
  services, or published packages.
- Expand product or architecture scope substantially.

## If Validation Fails

- Prefer a small corrective patch.
- Do not hide unrelated failures; summarize evidence and residual risk.
- Do not roll back broad areas unless the user asks or the exact safe rollback
  is clear.

