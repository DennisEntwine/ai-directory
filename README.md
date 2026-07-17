# AI Directory

A free, NL-first directory of AI tools, built around one defensible dataset: **which AI tools integrate with which platforms (CRMs, ERPs, marketing, sales, data), by what method, at what effort, and with which models**.

The directory is a neutral, trustworthy surface. The named expert behind it is **en:twine** ("Works by en:twine"), the AI agency that builds the middleware and intelligence on top of these tools. Lead generation to en:twine is the only monetization; the directory itself stays free.

- **Linear:** ENT-412 (business plan + roadmap, source of truth)
- **Status:** Phase 0 (scope, schema, and design direction)

## Repository layout

| Path | Owner | What lives here |
|------|-------|-----------------|
| [design/](design/) | Claude | Brand identity, design direction, tokens, and surface mockups (Phase 0 / 0.5) |
| [app/](app/) | Codex | The Astro 5 application (frontend built fresh on the reused en:twine stack) |
| [data/](data/) | Codex | Tool dataset as Zod-schema'd content collections, verification + refresh pipeline |
| [docs/](docs/) | Shared | Phase notes, decisions, and working plans |

## Ownership split

Per the Cortex ruleset:

- **Claude owns** design direction, design tokens, and the component system (see [design/brand/brand-direction.md](design/brand/brand-direction.md)).
- **Codex owns** the repo scaffold (Astro app), schema design, data pipeline, pSEO routing, lead-capture integration, and deployment.

## Stack (reused machinery, fresh frontend)

Astro 5 + React 19 islands + Tailwind v4 + shadcn primitives + Vercel + Supabase + PostHog. i18n NL/EN. Tool data as Zod-schema'd Astro content collections. Lead plumbing reused from the en:twine readiness-scan (`src/lib/readiness-scan/`). The **visual layer is entirely new**: own tokens, own component patterns, not entwine-website's brand.
