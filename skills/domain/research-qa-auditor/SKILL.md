---
name: research-qa-auditor
description: Use when auditing, implementing, or debugging equity research quality gates, especially stale periods, mixed snapshots, missing metric provenance, unsupported valuation thresholds, unclear current opinions, unrouted data gaps, industry-mismatched KPIs, color semantics, and pre-publish validation.
---

# Research QA Auditor

Use this skill before marking an equity research dossier, memo, dashboard, or
question response as ready.

## Audit Contract

A report is not ready if it has:

- stale fiscal periods, period-end dates, filing dates, price dates, or estimate
  dates;
- headline metrics without source, date, formula, or raw inputs;
- valuation thresholds without assumptions and calculation path;
- vague opinions without current view, evidence, trigger, and next watch item;
- fetchable or computable data gaps left as user-facing excuses;
- industry-mismatched KPIs or valuation methods;
- conclusions stronger than the evidence;
- misleading color semantics.

## Workflow

1. Identify the dossier snapshot: fiscal period, period end, filing/release
   date, price date, estimate date, currency, and data version.
2. Verify every module uses that snapshot or is explicitly marked stale.
3. Check every headline or conclusion-driving number for provenance.
4. Recompute important derived metrics when possible.
5. Verify alignment with the user's reason for following the stock.
6. Check opinion quality: current view, why, what would change it, next data,
   confidence, and evidence strength.
7. Convert non-user data gaps into executable research tasks.
8. Keep UI concise: conclusion first, formula/source/details on demand.

## Blocking Findings

- Missing coherent snapshot for real data.
- Stale current-quarter text.
- Key metric without provenance.
- Action threshold without formula and assumptions.
- Fetchable/computable/provider gap with no task.
- No clear current opinion.
- Known formula mismatch.

