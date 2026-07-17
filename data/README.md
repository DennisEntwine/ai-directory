# data/ (Codex-owned)

The tool dataset and its verification + refresh pipeline. **Not built yet** — placeholder marking the folder and its ownership.

## Shape

Tool data as **Zod-schema'd Astro content collections** (same pattern as the en:twine `blog` / `cases` collections). The dataset, not the page count, is the moat: which AI tools integrate with which platforms, by what method, at what effort, with which models.

## Taxonomy axes (multi-axis, from ENT-412 §3)

1. **JTBD** — the job the tool does.
2. **Integration surface** — native API / MCP / iPaaS / webhook / desktop-RPA / manual / none.
3. **Effort** — how hard the integration is.
4. **Underlying model** — which LLM(s) the tool runs on.
5. **Hosting / residency** — where it runs, data residency.
6. **Tags** — free-form secondary facets.

## Verification + refresh (data strategy, ENT-412 §13.4 — locked 2026-07-18)

Every record carries trust and freshness metadata, and **all data passes a verification flow regardless of origin** (self-sourced or user-submitted):

- `verified: boolean` — the gate. Flips `noindex` to indexable and unlocks the public record.
- `source` — where the record came from (self-sourced, submission, partner signal).
- `trust_tier` — `submitted` / `unverified` vs `verified`.
- `last_verified_at` — timestamp driving the **time-based refresh** (keep it simple: refresh on a cadence, re-verify, expire stale records).

**Refresh method is an open design task owned by Codex:** agent loop vs batch scrape + LLM diff vs checks against vendor API docs. The choice shapes these schema fields, so it is decided before the schema is frozen.
