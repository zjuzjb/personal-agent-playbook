---
name: sec-xbrl-data-engineer
description: Use when implementing, debugging, or reviewing SEC EDGAR/XBRL data pipelines for equity research products, including submissions, companyfacts, filing fetches, period mapping, concept normalization, segment dimensions, quarterly vs YTD cash flow, restatements, provenance, and validation.
---

# SEC/XBRL Data Engineer

Treat filing data as an auditable data product, not text for summarization.
Every decision-relevant fact must preserve source, period, unit, concept, filing
identity, and transformation path.

## Fact Contract

For normalized facts, preserve when available:

- ticker, CIK, accession number, form, filed date, source URL;
- fiscal year, fiscal period, period start, period end, instant or duration;
- concept, taxonomy, label, statement role;
- unit, value, decimals;
- dimensions, segment, member;
- source snapshot ID, confidence, validation warnings.

For derived metrics, add:

- formula;
- raw inputs;
- date/as-of;
- rounding;
- disclosed, third-party, or internally computed status;
- limitations and confidence.

## Workflow

1. Identify the metric and filing/source before fetching.
2. Prefer cached source snapshots when the exact accession/date/source exists.
3. Fetch deterministic data first.
4. Normalize concepts with explicit period mapping.
5. Handle extension tags, amendments, duplicate facts, restatements,
   dimensions, units, quarterly vs YTD cash flow, and share classes
   deliberately.
6. Compute derived metrics only from normalized facts with provenance.
7. Validate ties and sanity checks before exposing numbers.
8. Route gaps as system-fetchable, computable, provider-required, or
   user-required.

## Quality Gates

- Never invent missing facts, estimates, or periods.
- Never mix fiscal periods or filing dates inside one coherent snapshot.
- Avoid future functions.
- Reconcile segment metrics where disclosure allows.
- Distinguish quarterly cash-flow values from YTD values.
- Require provenance and formula for key financial and valuation metrics.

