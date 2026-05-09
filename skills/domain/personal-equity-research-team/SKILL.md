---
name: personal-equity-research-team
description: Design, review, or implement AI products that act as a personal equity research team for individual investors. Use for stock research workflows, watchlists, portfolio-aware thesis tracking, earnings review, catalysts, valuation, research memo UX, source/evidence architecture, user feedback loops, and incremental refresh.
---

# Personal Equity Research Team

Use this skill for products where an individual investor works with an AI
research team, not a one-shot report generator. Optimize for decisions,
continuity, evidence, traceability, and follow-up.

## Research Contract

Every visible research output should:

- Give a clear current view as of now.
- Explain why.
- Say what facts would change the judgment.
- Show what the team will watch next.
- Source every decision-relevant number with date, formula, period, unit, and
  provenance.
- Downgrade confidence or create a task when evidence is weak.
- Reflect the user's reason for following the stock.

## Product Questions

Map product work back to these questions:

- Why do I own or follow this stock?
- Has my thesis changed?
- Which evidence strengthens or weakens it?
- Is risk rising?
- Is valuation stretched or attractive?
- Did earnings change the setup?
- What catalysts should I watch?
- What important information did I miss?

## Durable Objects

Prefer continuous coverage objects:

- Coverage universe.
- Source vault.
- Research base.
- Question threads.
- Thesis scorecard.
- Financial model lite.
- Valuation snapshot.
- Catalyst calendar.
- Research team tasks.
- Analyst artifacts.
- Feedback loop.
- Cost and refresh log.
- Research snapshot.
- Metric provenance.
- Company profile classifier.
- Report QA result.

## Analyst Roles

- Research Director.
- Business Analyst.
- Financial Analyst.
- Valuation Analyst.
- Debate and Risk Analyst.
- Earnings Analyst.
- Catalyst Analyst.
- Editor.
- QA Auditor.

Keep tasks typed and scoped. Each task should have prerequisites, outputs, and
quality gates.

## Workflow

1. Identify the user decision being supported.
2. Identify the smallest durable research objects needed.
3. Decide which analyst role owns each object.
4. Define source prerequisites and missing-data behavior.
5. Design incremental refresh before full refresh.
6. Define the user review point.
7. Keep the UI conclusion-first, with supporting data on demand.
8. Add quality gates and tests before expanding scope.

## Anti-Patterns

- Long static reports when the user needs a decision checkpoint.
- Generic dashboards detached from investor questions.
- Fake data, fake estimates, fake sources, or untraceable numbers.
- Mixing stale fiscal periods, price dates, or estimate dates.
- Confident conclusions from weak evidence.
- Full refreshes when only one artifact changed.
- Cost-insensitive model calls.

