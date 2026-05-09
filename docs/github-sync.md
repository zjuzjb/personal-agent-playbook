# GitHub Sync Plan

This directory is ready to become a Git repository, but no GitHub repository has
been created yet.

Before creating the remote, decide:

- Repository name, recommended: `personal-agent-playbook`.
- Visibility: private by default unless there is a reason to publish.
- License: omit initially for private use, or choose one before making public.
- Whether `adapters/research-desk/` should be pushed or kept local.

Suggested local initialization after those decisions:

```bash
cd personal-agent-playbook
git init -b main
git add .
git commit -m "Initial personal agent playbook"
```

Suggested remote setup after creating the GitHub repository:

```bash
git remote add origin git@github.com:<user>/personal-agent-playbook.git
git push -u origin main
```
