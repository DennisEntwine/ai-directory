# app/ (Codex-owned)

The Astro 5 application. **Not scaffolded yet** — this is a placeholder marking the folder and its ownership.

## What Codex builds here

Clone the en:twine website **stack / machinery** for maintainability, then build the frontend **fresh** on Claude's design tokens and component system (do not copy entwine-website's components or brand):

- **Astro 5 + React 19 islands + Tailwind v4 + shadcn primitives** (restyled to the directory's own tokens in [../design/brand/tokens/](../design/brand/tokens/)).
- **i18n NL/EN** via the existing parity-test pattern (NL-first, EN later on the same schema).
- **Vercel** deploy, **PostHog** analytics.
- **Reuse the readiness-scan lead plumbing** from en:twine (`src/lib/readiness-scan/`: `notion-sales.ts`, `slack.ts`, email, `rate-limit.ts`, consent/PII) for the match-and-scope lead capture.
- **pSEO routing** with the data + demand gate: an indexable page exists only when a verified record exists (`verified: true` + min-content threshold flips `noindex` to indexable). Self-cleaning index.

## Boundary

Claude owns the design tokens and component system. Codex owns scaffold, schema, data pipeline, pSEO routing, lead capture, and deployment. Data lives in [../data/](../data/).
