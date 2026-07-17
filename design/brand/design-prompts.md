# toolfit — Claude Design prompts (ENT-548)

Aesthetic locked: **Technical-precise ("the wiring diagram")**. Paste the **BRAND CONTEXT** block at the top of every generation, then append one **SURFACE** prompt. Do the brand book first so the tokens stabilize, then reuse them for the surfaces.

---

## BRAND CONTEXT (paste at the top of every prompt)

```
Product: toolfit (toolfit.ai) — a free, bilingual NL+EN directory of AI tools. The moat is an
integration-compatibility dataset: which AI tools connect to which business platforms (CRMs, ERPs,
marketing, sales, data tools such as Exact, AFAS, Twinfield, Teamleader, Moneybird, HubSpot,
Salesforce), by what method (native API / MCP / iPaaS / webhook / desktop-RPA / manual / none), at
what effort, and with which underlying LLM. It is a neutral, trustworthy reference surface. It is
endorsed by, not branded as, the AI agency en:twine ("Works by en:twine").

Aesthetic: TECHNICAL-PRECISE, "the wiring diagram." Grid-locked layouts, structured whitespace,
monospace accents for data/method/endpoint fields. The signature motif is a NODE-AND-CONNECTOR graph:
small circular nodes joined by thin connector lines that literally depict an integration
(tool -> method -> platform). Motion is restrained: connector lines may draw in subtly on the hero
only; everything else is still. Authoritative and calm. NOT a kinetic startup look, NOT playful.

Palette (define as CSS custom properties in :root; no raw hex inside components):
  --color-bg #ffffff  --color-surface #fbfbfc
  --color-ink #14151a  --color-ink-muted #5b606b  --color-ink-subtle #8b909b
  --color-border #e6e8ec  --color-border-strong #cfd2d9   (thin rules = the wiring grid)
  --color-primary #c02338  --color-primary-hover #a11c2f  --color-primary-tint #fdeef0
     (RED = the single family tie to en:twine; use with restraint: brand mark, primary CTA, and the
      "live connection" accent on the node graph. Never decorative.)
  Integration-effort scale (functional, sits quietly in tables):
     native #1f8a5b  easy #4fa06b  moderate #c98a12  hard #c0562a  none #8b909b
  Trust: verified #1f8a5b  unverified #8b909b

Type: the brand's OWN system, NOT Manrope and NOT a default Inter/Roboto/Arial look. Display = a
grotesk with slight character; UI/body = a highly legible neutral sans; Mono = for method names,
endpoints, and effort. Modular type scale, body 16px minimum, rem units.

Build rules: semantic HTML5 (header/nav/main/section/article/footer/button/a), vanilla CSS with
custom properties (portable, ports to Tailwind v4 @theme later), mobile-first from 360px, WCAG 2.2 AA
contrast, visible :focus-visible rings, bilingual-ready (NL default + EN toggle; never assume text
width). Banned: purple gradients, glassmorphism, emoji-as-icon, fake 3D, generic SaaS hero with stock
art. Every color/space/radius/type value references a token.
```

---

## SURFACE 1 — Brand book (do this first)

```
Using the BRAND CONTEXT above, generate a single standalone brand-book web page (one semantic HTML
file + a :root token block) that documents the toolfit brand. Sections in order:
1. Cover: the toolfit wordmark with the node-and-connector motif rendered live.
2. Logo/wordmark usage + the "Works by en:twine" endorsement lockup (clear space, min size, don'ts).
3. Color system: swatches for base/ink/borders, the red primary, the integration-effort scale, and
   the trust colors; each swatch shows token name + hex + a one-line usage note.
4. Typography: display / UI / mono specimens and the full modular type scale with rem sizes.
5. The motif: the node-and-connector graph as a reusable element, with anatomy labels (node,
   connector, red "live-link"). Show a sample path: [CRM] -- MCP -- [LLM].
6. Components: primary/secondary button, tool card, compatibility badge, effort meter,
   filter chip, verified/unverified pill.
7. Voice: neutral-first, bilingual NL/EN example lines.
8. Do / Don't grid.
Grid-locked, monospace section labels, thin border rules between sections. Output the HTML + the CSS
token block.
```

## SURFACE 2 — Landing hero

```
Using the BRAND CONTEXT above, generate the toolfit landing-page hero at desktop 1440 and mobile 360.
Headline states the wedge — NL "Welke AI-tools passen in jouw stack." / EN "Which AI tools fit your
stack." One neutral subhead line on the integration-compatibility promise. Primary red CTA "Scan mijn
stack" / "Scan my stack". Visual: the node-and-connector graph showing a sample integration path
[CRM node] -- MCP -- [LLM node], with the connector line drawing in subtly on load (respect
prefers-reduced-motion). Persistent, unobtrusive "Works by en:twine" in header or footer. NL/EN
language toggle in the header. No stock imagery.
```

## SURFACE 3 — Catalogue + tool card

```
Using the BRAND CONTEXT above, generate the catalogue/browse surface. Left filter rail with the six
taxonomy axes as chips/checkboxes: job-to-be-done, integration surface (native API / MCP / iPaaS /
webhook / desktop-RPA / manual / none), effort, underlying model, hosting/residency, tags. Main area:
a responsive grid of tool cards. Each tool card: tool name + logo slot, one-line job-to-be-done, a row
of small compatibility badges (platform + method), an effort meter (native -> hard using the effort
scale colors), and a verified/unverified trust pill. Monospace for method labels. Mobile: the filter
rail collapses into a bottom-sheet triggered by a "Filters" button; no horizontal scroll.
```

## SURFACE 4 — Compatibility matrix (the centerpiece)

```
Using the BRAND CONTEXT above, generate the compatibility matrix surface. A dense, grid-locked table:
rows = AI tools, columns = business platforms (Exact, AFAS, Twinfield, Teamleader, Moneybird, HubSpot,
Salesforce). Each cell shows the integration method as a mono abbreviation (API / MCP / iPaaS / WH /
RPA / —) colored by the effort scale; an empty cell is a subtle gray "—" meaning no path. Sticky first
column and sticky header row. On mobile it scrolls horizontally without breaking layout (the first
column stays pinned). Include a legend mapping method abbreviations and effort colors. Treat each cell
as a "joint" in the wiring diagram — thin border rules, monospace, calm.
```

## SURFACE 5 — Match-and-scope flow + effort readout (headline lead magnet)

```
Using the BRAND CONTEXT above, generate the self-serve match-and-scope tool as a 3-step flow,
mobile-first: (1) pick the platforms you already run; (2) pick the outcome/job you want; (3) results.
The results screen shows each recommended tool as a node connected to the user's platforms (the
node-and-connector motif), an overall WORK-NEEDED readout (an effort meter plus a plain-language
estimate like "Moderate: roughly 2-3 days to wire up"), and a soft, non-pushy "Let en:twine build this
for you" CTA that opens a lead-capture form (name, work email, consent checkbox). Honest, neutral tone
— it should feel like a helpful estimate, not a sales funnel. Bilingual NL/EN.
```

## SURFACE 6 — Tool detail

```
Using the BRAND CONTEXT above, generate the tool detail page for a single AI tool: header with
name / logo / one-line job-to-be-done, a verified/unverified pill, and a "last verified" date; a
"connects to" node-and-connector diagram; a compatibility table (platform / method / effort / notes);
underlying-model and hosting/residency facts; and a light "Our take" opinion block that appears only
AFTER the neutral facts (end of page). "Works by en:twine" footer. Bilingual NL/EN.
```

---

### Usage notes
- Run **Surface 1** first; lock the tokens it produces, then feed those exact token values into the
  later prompts so the surfaces stay consistent (compose, don't regenerate).
- Keep the red disciplined: if a generation over-uses it, add "reduce red to the CTA and live-link
  accents only" and re-run.
- If a generation drifts into generic SaaS, add "more wiring-diagram: thinner rules, monospace data,
  visible node-and-connector structure" and re-run.
