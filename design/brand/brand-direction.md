# Brand direction (Phase 0)

Status: **draft direction.** Name and domain are the open decision that locks this doc. Palette family (red/white) is locked per ENT-412 §9a. Everything below is the proposed direction, ready to finalize once the name lands.

## 1. Positioning in one line

The neutral, NL-first map of which AI tools actually fit your stack, and how hard they are to connect. Built by the people who do the connecting: en:twine.

## 2. What the brand has to communicate

1. **Neutral and trustworthy.** This is a reference surface, not a sales page. It must read as an independent utility. That is the whole reason it can generate trust (and leads) for en:twine.
2. **Integration-first.** The wedge is not "list of AI tools." It is "what connects to what, by which method, at what effort." The visual system leans on structured data display: matrices, filters, effort readouts, compatibility badges.
3. **Dutch by default.** NL-first copy, NL examples, NL platform landscape (Exact, AFAS, Twinfield, Teamleader, Moneybird). Global EN comes later on the same schema.
4. **Quietly expert.** Neutral by default, light opinion only after the filters and analysis (end of page). The brand voice is calm and precise, not hypey.

## 3. Naming (open decision)

The repo working name is `ai-directory`. The product brand and domain are not yet locked. Directions on the table (see the decision surfaced to Dennis):

- **Dutch integration word.** "Koppeling" is the Dutch term for a software integration. A name playing on koppel / stack / fit reads native and is on-theme for the moat.
- **Descriptive SEO domain.** A literal `ai-tools`-style `.nl` domain trades brandability for pSEO strength on head terms.
- **Coined brandable.** A short, ownable coined word, distinct from en:twine, that can carry the "Works by en:twine" endorsement without confusion.

Decision criteria: (a) reads neutral, not like an en:twine sub-brand; (b) works in NL first and survives an EN expansion; (c) domain available; (d) does not fight the pSEO strategy.

## 4. Palette (locked family: red + white)

Red/white is the single shared anchor with en:twine. The directory's red is its **own** red, in the same family as en:twine's bordeaux but tuned for a data-dense utility (high legibility on dense tables, calm not loud). See [tokens/tokens.css](tokens/tokens.css) for the working values.

- **Base:** white / near-white surfaces, generous whitespace around dense data.
- **Ink:** near-black neutral for text, a cool gray ramp for structure (borders, table rules, muted labels).
- **Primary (red):** used with restraint. Reserved for the brand mark, primary actions, and the "Works by en:twine" lockup. Not for decoration.
- **Semantic:** integration-effort and compatibility states get their own restrained scale (for example: native / easy / moderate / hard / none). These are functional colors, tuned to sit quietly inside tables.

## 5. Typography (own, not borrowed)

Fresh type, deliberately not en:twine's Manrope.

- **Display / wordmark:** a grotesk with a little character for the logo and page headers.
- **UI / body:** a highly legible neutral sans for dense tables and filters (Inter or an equivalent is the working default).
- **Mono:** for API method names, endpoints, and code-ish integration fields.

Final faces are picked in the Phase 0.5 mockups, once the name (and therefore the wordmark) is set.

## 6. Voice

Calm, precise, Dutch-first, low on adjectives. States facts about tools and integrations, then offers a light recommendation only after the analysis. Never breathless. The "Works by en:twine" line is a quiet signature, not a banner.

## 7. What is explicitly NOT inherited from en:twine

- Not en:twine's components or component library.
- Not its exact brand colors beyond the red/white family tie.
- Not its typography.
- Not its layout system.

Reused: the **tech stack / machinery** and the **backend lead plumbing** only. See [../../app/README.md](../../app/README.md).
