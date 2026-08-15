# Interoperability map: context and identity formats for AI

> Part of the [.contexto/](README.en.md) standard. Second edition. Compares the living formats that encode identity or context for an AI to operate. First edition: 2026-07-27, four personal context formats. This edition: 2026-08-15, adding the family of brand identity standards and the institutional layer that appeared in between. Spanish version: [interoperabilidad.md](interoperabilidad.md).

The map covers the whole category: what each format solves, where `.contexto/` is weaker than the others, and where the others are weaker among themselves. When a source could not be verified in detail, the document says so instead of filling the gap by analogy.

Each format's absences are named in two distinct categories, because they are distinct things: **pending**, when the format acknowledges the gap and is on its way to covering it, and **excluded by design**, when the absence is a thesis decision with its reason stated. This distinction applies `.contexto/`'s honest-states principle to the standard itself.

## What changed since the first edition

In three weeks the terrain went from one family to three.

An entire family of agent-readable brand identity standards was born: the Brand Context Protocol by Encoded Brands, `brand.md`, `brandbook.md`, `brandkit.md`, and several more listed below. None of them existed in the July map.

An institutional layer appeared above all of them: Google Cloud's Open Knowledge Format, which standardizes knowledge bundles in markdown with frontmatter, and AGENTS.md, now under the Agentic AI Foundation at the Linux Foundation.

And of the four original formats, two moved and two did not: Creed ships daily, while Whittemore's portfolio has not received a single commit since March 26, even as it kept collecting stars.

## 1. The terrain in three layers

These formats do not all compete with each other. They answer different questions, and separating them before comparing is worth the trouble.

**Context of a person.** What an AI needs to know to work with someone: `.contexto/` in person mode, personal context portfolio, Creed and me.md.

**Identity of a brand.** What an AI needs to know to write, design or speak on behalf of a brand: `.contexto/` in brand mode, Brand Context Protocol, `brand.md`, `brandbook.md`, `brandkit.md`, and at the edge `brand.yml`, `DESIGN.md` and `brandspec`, which solve the visual and token layer.

**Knowledge and instructions of an organization.** What an organization knows and how its code is operated: Open Knowledge Format and AGENTS.md. They encode material and procedure, and they combine with either of the two layers above.

`.contexto/` spans the first two layers with the same structure: its unit is the subject who decides, and a person and a brand are two kinds of subject.

## 2. Equivalence table: person as subject

| Dimension | `.contexto/` | personal context portfolio | Creed | me.md |
|---|---|---|---|---|
| **Identity** | `identidad.md`: why the work exists, what world it pushes for, what it must not lose. For people it adds "current moment" | `identity.md`: one page, the minimum file if an agent can only read one | **Identity** section (fixed): role, stable traits, defaults that follow the person everywhere | Not verifiable as its own section; the public example shows "Quick Load", with a similar function |
| **Role / work** | `rol.md` (v1.1): what they actually do versus what the title says, the typical week, with whom, what they decide, what they delegate | `role-and-responsibilities.md`: what the weeks look like in practice | **Work** section (fixed): profession, tools, methods, collaborators | Not publicly verifiable |
| **How they decide** | `logica.md`: case law with dates, derived rule, and explicit precedence between colliding rules | `decision-log.md`: how they decide, two or three real decisions with the reasoning | Partial, **Beliefs** section (optional). No cases, no precedence | Mentioned as a captured category, with no visible section or example |
| **Voice / style** | `formas.md`: synthesis, yes-like-this / not-like-this samples with quoted phrases, prohibitions with their replacement, tone by context | `communication-style.md` | **Preferences** section (fixed): tone, length, depth, format | Partially confirmed: a "Communication" section plus writing cards |
| **Relationships** | `audiencias.md`, with a side note for people without their own market | `team-and-relationships.md`: fields per person | **People** section (optional), with concrete examples per person | Not publicly verifiable |
| **Goals** | `identidad.md` for the horizon and `rol.md` for current priorities, including "what I am NOT prioritizing" with the tradeoff for each renunciation (v1.1) | `goals-and-priorities.md`: includes tradeoffs and what is not being prioritized | **Goals** section (fixed), with examples of what counts and what does not | Not publicly verifiable |
| **Constraints** | `restricciones.md`: what it would never do, operating conditions, promise states | `preferences-and-constraints.md`: hard rules, personal constraints | **Constraints** section (optional): limits and topics requiring permission | Mentioned as "boundaries", no confirmed section |
| **History / cases** | The strongest of the four: `logica.md` plus `evidencia.md` plus `verificacion.md` | `decision-log.md`, "Recent Decisions" block, with no mandatory date or derived rule | Excluded by design: the agent contract rules out single-conversation notes | Not verifiable; the model is cards, not narrated cases |
| **Permissions / governance** | Excluded by design: one owner and their AI. Integrity solved in v1.1 with documented `SHA256SUMS` | Not covered | The strongest: four levels per section, three roles on the Company plan | Partial: control over what is shared on export, plus a SHA-256 seal |
| **Updating** | `feedback.md` plus versioning of the standard itself. Manual process | No formal mechanism | The most automated: agents propose edits continuously, the owner approves, two-way GitHub sync | Progressive questionnaire, "Pack v1" format still closed |
| **Project movement** | Last release 2026-08-15. 0 stars | No commits since 2026-03-26. 454 stars, 305 forks | Daily development, last push 2026-08-14. 166 stars | Product at v0.1, no public repository |

## 3. Equivalence table: brand identity

| Dimension | `.contexto/` | Brand Context Protocol | brand.md | brandbook.md |
|---|---|---|---|---|
| **Root** | `guia.md`: reading order, operating rules, declared omissions | `/.well-known/brand.md`: identity, core positioning and daughter registry | Single file with frontmatter (`name`, `tagline`, `version`, `language`, `specVersion`, `type`, `architecture`) | `BRANDBOOK.md` as an index of thematic files |
| **Strategy** | `identidad.md` plus `territorio.md` plus `arquitectura.md` | Positioning at the root, values in `values.md` | Mandatory **Strategy** layer: overview, audience, positioning, personality, references and anti-references, promise, guardrails | Audience and context files |
| **Voice** | `formas.md` | `voice.md` plus `voice/anti-ai.md` for generated-language patterns | **Voice** layer: identity, taglines, manifesto, message pillars, phrases, vocabulary, tonal rules | Voice file |
| **Visual** | `visual.md`, with the rule of declaring the absence when there is no system | `visual.md` plus optional extensions (`tokens.json`, `tokens.css`, `DESIGN.md`) | **Visual** layer: logo, core colors, typefaces, imagery, art direction | Assets file |
| **Limits** | `restricciones.md`, with promise states | `boundaries.md`: categorical hard nos and soft nos with their condition | `guardrails` inside Strategy, with inheritance that hardens and never weakens | Governance file |
| **Claims** | `evidencia.md`: claimable, not claimable, permitted promises | `claims.md`: claim, evidence, `proof_status` (approved, requires_caveat, forbidden, expired, aspirational, unknown), `valid_from` and `valid_until` | **Claims** in Governance: only human-approved statements or ones backed by cited proof | Numbered anchor rules |
| **How a third party describes you** | `representacion.md` (v1.1): approved descriptions in three lengths, what it gets confused with, what never to say, comparisons, framing traps | `representation.md`: approved descriptions by length, what not to confuse the brand with, what never to say, who it really competes against | Not covered | Not covered |
| **Discovery** | Partial: publishes `representacion.md` at a well-known location, linked and mirrored in structured data, and declares that the well-known location has no consumers yet. The rest of the folder stays private on purpose | Solved: well-known URL on the domain, plus a hosted registry that signs the files and serves them over MCP | Directory inheritance within a project | Not verified in detail |
| **Precedence** | Between colliding rules, by content and with its condition | Between files, by hierarchy: campaign, product, audience, locale, default daughter, root | Between parent and child: guardrails merge, the child hardens | Cross-references between sections |
| **State and freshness** | Honest states per field, including declared emptiness, plus provenance and expiry frontmatter per file (v1.1) | Three conformance levels, `last_updated` per file, validity dates on claims | `specVersion` as a validation gate, integer `version` incrementing | Software-style versioning |
| **Verification** | `verificacion.md`: cases any AI can run, with the expected response and the rule that justifies it. Plus `auditoria.md`, a prompt that audits the folder against the principles | Technical conformance: reachable URI, valid markdown and YAML, reachable daughters | Validation against the declared spec version | Not verified in detail |
| **Learning** | `feedback.md`: every correction from the owner with date, rule and example | Not covered in the spec as read | Not covered | Not verified in detail |
| **License and model** | CC BY 4.0, a convention with no infrastructure | CC BY 4.0 for the spec, MIT for the reference code, with a commercial subscription registry | MIT | CC BY 4.0 for the spec, MIT for the code |

At the edge of this family there are three more formats that solve the visual and token layer before full identity: `brand.yml`, `DESIGN.md` (from Google Stitch) and `brandspec`. They are named because they appear in the category's landscape; they were not read in detail for this edition and nothing is claimed about their contents.

## 4. The dimension no format covers

Of the twelve formats reviewed for this edition, none encodes where the subject looks.

All of them solve expression: how it sounds, how it looks, what it can claim, what limits it has, how a third party should describe it. None solves attention: what fields it observes, how the world reaches it, what lens it reads a new fact through, and what it does with what it sees.

The consequence is structural and can be stated precisely: when every file in a folder describes the subject, the only material available for producing anything is the subject itself. An encoded identity without attention can hold its tone indefinitely and can only talk about itself.

The reference implementation of `.contexto/` has been running `mirada.md` since 2026-08-13, with fields of attention derived from the slow documents, declared sources of world, a lens of questions that orders the reading of any finding, and the signals that would force a revision of its own thesis. Until other formats take it up, this row is empty for the other eleven.

## 5. Two distinctions that look like the same thing

**Validating format and verifying behavior.** The Brand Context Protocol declares conformance when the file sits at the right URI, the markdown and YAML are valid, and the daughters are reachable. `verificacion.md` in `.contexto/` runs situations and compares the answer against the expected one, with the rule that justifies it. The first checks that the container is well built; the second, that the identity is being operated. A file can be perfectly conformant and still produce output that betrays the subject.

With the same honesty: the `.contexto/` suite verifies fidelity to what is declared, using cases written in the folder itself. Verifying judgment, with held-out cases outside the folder and blind comparison, is a second form that no format in the category implements yet, this one included.

**Precedence between files and precedence between rules.** BCP resolves which file wins when two apply: a campaign daughter overrides a product one, which overrides the root. `.contexto/` resolves which rule wins when two of the subject's principles collide, with its explicit condition, and it allows recording an unresolved tension when the owner holds both positions. These are different problems: one is scope resolution, the other is value conflict.

## 6. What each format has that the others do not

### `.contexto/`

Has: nine explicit, auditable principles with a runnable audit prompt. Case law with case, date and derived rule, the strongest dimension in the whole category. Precedence between conflicting rules, including the option of holding a tension without averaging it. The honest-states rule, where declared emptiness counts as legitimate content. The declared-omission rule, which the Sole example demonstrates by omitting three files. A behavior verification suite. A file that grows with the owner's corrections. It is the only one of the twelve native to Spanish, and the only one using the same structure for a person and for a brand.

**Solved in v1.1 (2026-08-15):** `mirada.md` for attention, `rol.md` with the "what I am NOT prioritizing" category and its tradeoffs, `representacion.md` for third person, provenance and freshness frontmatter per file compatible with the Open Knowledge Format, and integrity through documented `SHA256SUMS`.

**Pending:** inheritance between parent brand, product and sub-brand. Judgment verification with held-out cases, which no format in the category has. And full discovery: the third-person material is published at a well-known location, while the rest of the folder still travels by hand, which is a privacy decision more than a gap.

**Excluded by design:** multi-agent governance and per-section permissions, which belong to team products and which Creed solves well. Its own infrastructure: automatic sync, scoring as a service or a dedicated connector, because the standard is a neutral file convention and the tools that operate it are another layer, one per implementer.

### Brand Context Protocol (Encoded Brands)

Has, by a wide margin over the rest of the family: discovery solved through a well-known URL, so a third party's agent can read the brand without anyone handing it over. A hosted registry that signs the files and serves them over MCP. Three declared conformance levels. Hierarchical precedence between files by campaign, product, audience and locale. `proof_status` with six values and validity dates on every claim, with an explicit policy on named entities. A dedicated file for AI-generated language patterns, with type, pattern, rationale and example. And `representation.md`, with no equivalent in any other format read.

Does not have: cases with dates or case law. Behavior verification. Accumulated learning from owner corrections. Any notion of field state beyond claims. And the public spec was at v0.7 while the company's own file already declared v0.8, so it is worth reading both when integrating.

### brand.md (Caio Pizzol)

Has: the cleanest formulation of inheritance between parent brand, product and sub-brand, with the rule that a child may harden a guardrail and never weaken it, and that accessibility commitments always merge upward. `specVersion` as a validation gate, with defined behavior for a file that does not declare it. References and anti-references as a mandatory strategy field. MIT license and a single file, the lightest entry in the family.

Does not have: cases, dates, case law, runnable verification, per-field completeness states, or a representation layer. It declares which languages it supports, and Spanish is not among them.

### personal context portfolio (Whittemore)

Has: the richest dedicated files in the category for role and for relationships, and the most explicit formulation of "what I am not prioritizing right now". Three complete example people. An entire directory devoted to integrations. MIT license.

Does not have: governance, dates, versioning, precedence, verification or field states. And it has not received a commit since March 26, though it remains by far the most adopted, with 454 stars and 305 forks.

### Creed

Has: real per-section permissions with its own testable logic module, active GitHub sync, AI quality scoring of the file, MCP connection with OAuth and flows for more than ten agents. Two sections with no equivalent anywhere else: Routines and Health. It is the most actively developed project of all those reviewed.

Does not have: case law or dated cases, excluded by design. Field states. Runnable verification. Territory or "who it is not for". And in its hosted form it is a product with paid plans.

### me.md

Verifiable: measurable, communicated progression by number of cards answered, a SHA-256 seal on the exported file, sensitivity control when sharing, and a category of technical cards turned off by default. The lightest entry in the whole category.

Does not have, or could not be verified: a published section schema, an auditable repository, or public evidence of how it covers role, relationships, goals or history. The claim is not that it lacks them; the claim is that it cannot be verified from outside.

### Open Knowledge Format and AGENTS.md

These sit in another layer and comparing them head-on is misleading. OKF standardizes knowledge bundles with frontmatter answering three questions no identity format was asking: where this came from (`sources`), who produced it and who confirmed it (`generated`, `verified`), and whether it is still current (`status`, `stale_after`). AGENTS.md standardizes project instructions for coding agents and is adopted across more than sixty thousand repositories.

Neither encodes a subject. The useful reading is one of fit: a knowledge bundle does not say who is speaking, and an identity folder does not say what the organization knows. A complete subject will need both, and expressing `.contexto/` states in OKF-compatible frontmatter is the shortest path for ecosystem tooling to read an identity folder without integration work.

## 7. Migration notes

### From personal context portfolio to `.contexto/`

`identity.md` maps directly onto `identidad.md`, but its originating case has to be added: `.contexto/` does not accept self-definition without a case, and `identity.md` is written as a summary rather than a scene. `communication-style.md` is rewritten as `formas.md`, adding yes-like-this / not-like-this pairs with genuinely quoted phrases. `team-and-relationships.md` compresses into `audiencias.md`; the per-person structure is lost unless the fields are replicated by hand. `decision-log.md` splits between `logica.md` and `evidencia.md`; each decision needs a date and an explicit operating rule that `decision-log.md` does not require.

Reverse path: `logica.md` and `evidencia.md` merge into a single `decision-log.md`, losing the separation between rule with precedence and verifiable case.

### From Creed to `.contexto/`

Identity, Work and Preferences split across `identidad.md`, `arquitectura.md` and `formas.md`; cases and dates have to be added, because Creed's contract forbids exactly the task-level detail that `.contexto/` requires as proof. Goals pours into `identidad.md`. Constraints migrates directly to `restricciones.md`, classifying each rule as current, lab, horizon or history. The per-section permission model has no destination: multi-agent governance is excluded by design. If a case needs per-agent, per-section permissions, Creed is the right format today.

Reverse path: `identidad.md`, `formas.md` and `restricciones.md` flatten into Creed's fixed sections, losing the case law with dates and derived rules.

### From me.md to `.contexto/`

With what is verifiable today, only "Quick Load" and "Communication" can be migrated with confidence, into `formas.md`. Boundary cards would migrate to `restricciones.md`. The rest cannot be mapped responsibly without access to the full schema: better to declare the gap than to invent a destination.

### From Brand Context Protocol to `.contexto/`

`voice.md` maps to `formas.md`, and `voice/anti-ai.md` enters as a prohibitions block inside the same file, keeping the per-class typing, which is finer-grained than `.contexto/`'s. `values.md` splits: the decision rules go to `logica.md` and need their originating case and date added, which BCP does not ask for; the collision rules are already precedence and migrate almost verbatim. `boundaries.md` goes to `restricciones.md`, and soft nos with conditions fit the operating-condition format directly. `claims.md` goes to `evidencia.md`, mapping `proof_status` onto promise states: approved to current, aspirational to horizon, requires_caveat to partial input. `visual.md` maps to `visual.md`. `representation.md` maps to `representacion.md`, which is the closest one-to-one match between the two formats.

Reverse path: `logica.md` loses its cases and dates when flattened into collision rules, and `verificacion.md` and `feedback.md` have no destination in BCP. In exchange you gain discovery and signing, which `.contexto/` does not provide.

## 8. Sources

Reading date for this edition: 2026-08-14 and 2026-08-15. The first edition read the four personal formats on 2026-07-27 and its sources remain listed below. Anything not listed here was not read for this map.

**Brand Context Protocol / Encoded Brands** (read 2026-08-14):
- Full v0.7 specification at `brandcontextprotocol.dev/spec/v0.7/`
- `encodedbrands.ai/.well-known/brand.md` (the actual root file, declaring `bcp_version` 0.8 and `last_updated` 2026-08-05)
- Actual daughter files: `voice.md`, `voice/anti-ai.md`, `values.md`, `boundaries.md`, `claims.md`, `representation.md`
- `encodedbrands.ai` (home, commercial model and plans)
- Repository metadata for `github.com/Brand-Context-Protocol/spec` via `gh api`: organization created 2026-05-04, last push 2026-08-10, 1 star
- Not read: `visual.md`, `commerce.md`, or the optional extensions

**brand.md** (read 2026-08-14):
- Complete `spec/brand-md.md`, version 0.3.0, at `github.com/caiopizzol/brand.md`
- Repository metadata via `gh api`: created 2026-03-13, last push 2026-08-05, 22 stars, 4 forks, MIT license
- The author's public profile and `caiopizzol.com`

**brandbook.md** (read 2026-08-14):
- `brandbook.md/` (home: file structure, licenses, draft 0.1 status)
- `brandbook.md/landscape/` (its own comparison of eight brand standards)
- Repository metadata: organization `brandbook-md`, created 2026-07-16, 0 stars
- The specification was not read file by file

**brandkit.md** (read 2026-08-14): `README.md` of `github.com/360vier/brandkit.md`, v0.1.0-draft. Metadata via `gh api`: created 2026-03-13, last push 2026-03-14, 1 star, MIT.

**Open Knowledge Format** (read 2026-08-14): complete `okf/SPEC.md` v0.2 at `github.com/GoogleCloudPlatform/knowledge-catalog`, the Google Cloud announcement, and secondary coverage for the v0.1 (2026-06-12) and v0.2 (2026-07-25) dates.

**AGENTS.md** (read 2026-08-14): secondary coverage only, for its institutional status and declared adoption. The specification was not read.

**Discovery and adoption** (read 2026-08-15): [RFC 8615](https://www.rfc-editor.org/rfc/rfc8615.html) for the well-known URI prefix and its IANA registry; public measurements of `llms.txt` adoption, including the SE Ranking study of 300,000 domains and the reported 408 hits across 500 million AI bot visits over ninety days; and the stated positions of Google, OpenAI and Anthropic on reading such files.

**Status of the four personal formats as of 2026-08-14**, verified via `gh api`: personal context portfolio 454 stars, 305 forks, last push 2026-03-26; Creed 166 stars, last push 2026-08-14; `.contexto/` 0 stars. me.md content re-read at `getmemd.com`.

**Not verified in this edition:** `brand.yml`, `DESIGN.md` and `brandspec`, named in section 3 with no claims about their contents. The two other initiatives using the Brand Context Protocol name, from Aryabhatta Labs and from Wild, which appear in brandbook.md's landscape and were not read. Creed's current changelog, whose public file points to an internal module of the repository that was not opened.
