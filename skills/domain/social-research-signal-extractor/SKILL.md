---
name: social-research-signal-extractor
description: Extract grounded investment research signals from authorized social media posts, investor comments, expert notes, channel checks, forum threads, or user-provided text. Use to separate facts, observations, opinions, rumors, evidence snippets, value level, verification tasks, and routing decisions.
---

# Social Research Signal Extractor

Convert noisy social or expert commentary into durable research signal objects.
Do not summarize a feed. Extract claim cards that can enter a research workflow,
verification queue, thesis review, tracker, or archive.

## Rules

- Process only authorized, user-provided, licensed, or otherwise permitted text.
- Preserve source grounding. Every non-discard claim needs an evidence snippet.
- Extract claims, not prose summaries.
- Separate fact, first-hand observation, hearsay, author inference, rumor, and
  emotion.
- Do not convert opinion into fact or rumor into evidence.
- Entity-link by role: primary, comparison, mentioned, quoted, or source noise.
- Route weak content to discard or archive.

## Workflow

1. Source gate: authorized, user-provided, licensed, public-allowed, unknown, or
   blocked.
2. Normalize author, timestamp, source, URL, raw text, quote/repost text, and
   available engagement.
3. Discard non-investment, low-information, or weakly matched content.
4. Link companies, industries, products, people, themes, and metrics.
5. Split into atomic grounded claims.
6. Mark evidence type and confidence.
7. Score value as high, medium, low, or discard.
8. Generate verification tasks for high and medium claims.
9. Route to verification queue, stock signal pool, industry tracker, thesis
   review, daily digest, archive, or discard.

## Quality Checks

- Every claim has exact evidence or is discarded.
- Tickers are not assigned because of source noise or quoted-only context.
- High-value claims have verification tasks.
- Claims do not add causal language absent from evidence.
- Source rights and retention assumptions are explicit when unclear.

