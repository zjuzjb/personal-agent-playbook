---
name: plan-todo-manager
description: Maintain a living development plan and TODO backlog for coding projects. Use when the user asks to plan work, rank priorities, continue by plan order, preserve future tasks, move chat decisions into docs, update TODOs, avoid losing long-context decisions, or keep old implementation debt from accumulating.
---

# Plan TODO Manager

Use this skill to keep project execution ordered, durable, and clean. The goal
is not to write a long plan; it is to make sure important decisions, active work,
and future backlog do not disappear in chat history.

## Habits

- Keep a single living plan document when the repo has one, usually `TODOS.md`,
  `TODO.md`, `ROADMAP.md`, or a project-specific planning doc.
- If no plan doc exists and the task is non-trivial, create a concise planning
  doc in the project root.
- Put new tasks into the right priority tier instead of appending blindly.
- Work in plan order unless a blocker or user priority justifies reordering.
- Move valuable chat decisions into docs before context gets long.
- After finishing a slice, update its status and next step.
- Put useful later work in backlog without interrupting the current path.
- When new behavior replaces old behavior, plan cleanup for obsolete code,
  data paths, demos, stale copy, and compatibility shims.

## Priority Shape

- `P0`: correctness, safety, data integrity, build/test blockers, user-blocking
  bugs.
- `P1`: core product behavior and architecture for the current milestone.
- `P2`: UX polish, performance, quality improvements, charts, automation.
- `Backlog`: useful later work.

Each active item should have status, change summary, scope, acceptance, and
durable notes if needed.

## Workflow

1. Find the plan doc with `rg --files | rg '(TODO|TODOS|ROADMAP|PLAN|BACKLOG)'`.
2. Read only relevant sections.
3. Merge the user request into the right priority.
4. Before multi-step implementation, update the active plan.
5. Keep the live task plan aligned with the document plan.
6. After implementation, update status and verification evidence.
7. Move unfinished follow-ups to the right priority or backlog.

## Output Discipline

- Do not ask the user to maintain the plan manually.
- Do not let the plan become a changelog.
- Do not preserve obsolete implementation paths just because they exist.
- Do not claim completion without verification or explicit inspection.

