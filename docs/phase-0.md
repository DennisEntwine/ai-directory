# Phase 0 — Scope, schema & design direction

Source of truth for the business plan is **ENT-412**. This file tracks Phase 0 execution in the repo.

## Phase 0 deliverables (from ENT-412 §9)

- [x] **Lock domain / brand (working title)** — **`toolfit` / `toolfit.ai`**, alt `toolfuse.ai`. Domain `.ai` (not `.nl`); **bilingual NL+EN from day one**, NL market primary. Palette family (red/white) locked. Final lock pending EUIPO/BOIP trademark check.
- [x] **Brand identity + design direction** — set in [../design/brand/brand-direction.md](../design/brand/brand-direction.md) + [../design/brand/tokens/tokens.css](../design/brand/tokens/tokens.css). Wordmark finalizes in Phase 0.5 mockups.
- [ ] **Draft content-collection schema** — Codex, with the `verified` / `source` / `trust_tier` / `last_verified_at` fields from §13.4. Blocked on the refresh-method design choice.
- [ ] **Choose seed categories** — the first slice of the catalogue (NL platform landscape first: Exact, AFAS, Twinfield, Teamleader, Moneybird, plus the common AI tools that connect to them).
- [ ] **Decide refresh method** — Codex (agent loop vs batch scrape + LLM diff vs vendor-doc checks).

## Then Phase 0.5 (design gate)

Claude mocks the five key surfaces in Pencil (see [../design/mockups/README.md](../design/mockups/README.md)), reviewed before any Phase 1 build.

## Ownership

- **Claude:** domain/brand direction, design tokens, component system, surface mockups.
- **Codex:** content-collection schema, seed-category data model, refresh-method design, repo/app scaffold.

## Open decisions

1. **Brand name + domain** — resolved to working title `toolfit.ai` (alt `toolfuse.ai`). Remaining: EUIPO/BOIP trademark check before buying + final lock.
2. **Refresh method** (Codex) — blocks freezing the schema fields.
