# Portability Guide

## For A New Project

1. Copy `templates/AGENTS.project.md` into the project as `AGENTS.md`.
2. Add project docs only for rules that are specific to that project.
3. Copy core skills only when the project needs them.
4. Create an adapter if the project has custom issue flow, review states, or
   domain constraints.
5. Keep product facts out of global rules.

## For An Existing Project

1. Inventory existing project rules.
2. Classify each rule as core, domain, adapter, reference, or exclude.
3. Move only generalized rules into this playbook.
4. Leave project-specific rules in the project.
5. Add adapter notes if the project needs a repeatable overlay.

## Sync To GitHub Later

Before creating a GitHub repository, decide:

- Repository name.
- Visibility: public or private.
- License, if any.
- Whether to push all adapters or keep private project adapters local.
- Whether to include install scripts in the first commit.

