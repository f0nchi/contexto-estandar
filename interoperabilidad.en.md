# Interoperability map: personal context files for AI

> Part of the [.contexto/](README.md) standard. Compares the four live formats that encode personal identity or context for an AI to operate: `.contexto/`, personal context portfolio, Creed and me.md. All four sources read on 2026-07-27. Versión en español (canónica): [interoperabilidad.md](interoperabilidad.md).

This map is not a brochure for `.contexto/`. It is a map of the category: it includes where `.contexto/` is weaker than the other three, and where the other three are weaker among themselves. Where a source could not be verified in detail, the document says so instead of filling the gap by analogy.

Each format's absences are named in two distinct categories, because they are distinct things: **pending** (the format acknowledges the gap and it is on its way) and **excluded by design** (a thesis decision, not a shortcoming). This distinction applies the honest-states principle of `.contexto/` to the standard itself.

## The four formats, one line each

- **`.contexto/`** (Ideas Aumentadas, f0nchi): an open convention in Spanish, twelve plain-text files (eleven core plus `feedback.md`), seven auditable principles, with templates and a complete example. Repository: `github.com/f0nchi/contexto-estandar`.
- **personal context portfolio** (Nathaniel Whittemore): ten markdown files in English, each with an embedded interview protocol so an AI assistant can draft it with the owner. MIT license. Repository: `github.com/nlwhittemore/personal-context-portfolio`, 447 stars.
- **Creed** (connorhpbrn): a SaaS product (Next.js plus Supabase), one `creed.md` file per person with ten sections (five fixed, five optional) and per-section write permissions for every connected agent. Repository: `github.com/connorhpbrn/creed`, 149 stars.
- **me.md** (Aprex, Norway, `getmemd.com`): a closed-source product with no known public repository (one was searched for and not found). A multiple-choice card questionnaire that compiles an exportable personal README. Structure only partially verifiable: see the note in section 1 and in the sources.

## 1. Equivalence table

| Dimension | `.contexto/` | personal context portfolio | Creed | me.md |
|---|---|---|---|---|
| **Identity** | `identidad.md`: why this work exists, what world it pushes toward, what it must never lose. For individuals it adds a "current moment" block | `identity.md`: one page, the minimum file if an agent can only read one | **Identity** section (fixed): role, stable traits, defaults that follow the person everywhere | Not verifiable as a section of its own. The public example shows "Quick Load", similar in function, without confirming it is the formal equivalent |
| **Role / work** | Pending (lands in v1.1 as a dedicated file for role and weekly operation). Today `identidad.md` touches the why of the work, not the week | `role-and-responsibilities.md`: what weeks actually look like, not what the formal title says | **Work** section (fixed): profession, tools, methods, recurring collaborators | Not publicly verifiable |
| **How decisions are made** | `logica.md`: dated case law, the rule each case left, and explicit precedence when two rules collide | `decision-log.md`: how they decide, what they need before deciding, two or three real decisions with the reasoning, how they handle uncertainty | Partial, **Beliefs** section (optional): values and principles that change how the AI should reason. No cases, no precedence | Mentioned as a captured category ("decision style") on the product home, with no visible section or example |
| **Voice / style** | `formas.md`: synthesis, real "like this / not like this" samples with quoted phrases, prohibitions each with its replacement, tone by context | `communication-style.md` | **Preferences** section (fixed): tone, length, depth, response format | Partially confirmed: a "Communication" section in the public example plus writing cards ("would rather sound a bit blunt than overpolished") |
| **Relationships** | `audiencias.md`, with a side note for individuals without a market of their own. Reuses the market-audience structure; no per-person fields | `team-and-relationships.md`: per-person fields (role, how they interact, what each needs from the other) | **People** section (optional), with concrete per-person examples in the agent contract itself | Not publicly verifiable |
| **Goals** | Partial, inside `identidad.md`, "current moment" block: open fronts, one-year horizon. The explicit "what I am NOT prioritizing" category is pending: lands in v1.1 | `goals-and-priorities.md`: includes how tradeoffs get resolved and what is NOT being prioritized | **Goals** section (fixed), with explicit examples of what counts and what does not count as a goal | Not publicly verifiable |
| **Constraints** | `restricciones.md`: what they would never do, operating conditions, promise states (current, laboratory, horizon, history) | `preferences-and-constraints.md`: hard rules, pet peeves, personal constraints | **Constraints** section (optional): lines the AI must not cross, topics that require explicit permission | Mentioned as a captured category ("boundaries"), no confirmed section |
| **History / cases** | The strongest of the four on this dimension: `logica.md` (dated case law) plus `evidencia.md` (claimable / not claimable) plus `verificacion.md` (test cases any AI can run) | `decision-log.md`, "Recent Decisions" block: two or three real examples, no mandatory date, no explicit derived rule | Explicitly outside the model: the agent contract excludes "task-level trivia" and single-conversation notes by design | Not verifiable. Probably does not apply: the model is choice cards, not dated narrative cases |
| **Permissions / governance** | Excluded by design: the model is one owner and their AI, no seats, no access levels (see section 2). Under evaluation for v1.1: an integrity seal on the exported file | Not covered. No file or `wiring/` guide defines permissions or change approval | The strongest by far: `lib/creed-permissions.ts`, four levels per section (hidden, read-only, propose, direct), three roles on the Company plan (owner, admin, member) | Partial: no per-section permissions, but export-time control of what gets shared (sensitivity level, per-item toggle) and a SHA-256 integrity seal on the file |
| **Updating** | `feedback.md` (date, learned rule, example; manual process) plus versioning of the standard itself (v1.0, changelog with date and rationale) | No formal mechanism. One declared principle: "update regularly" | The most automated: agents propose edits continuously, the owner approves, two-way GitHub sync, AI-driven quality scoring of the file | Progressive questionnaire (first signal at 5 cards, useful export at 40, deep profile at 200), product at v0.1, "Pack v1" format still closed |

## 2. What each format has that the others do not

### `.contexto/`

Has: seven explicit, auditable principles, with a runnable audit prompt (`auditoria.md`) that any AI can execute against the folder itself. Explicit precedence when two rules collide. The "honest states" rule: every field declares whether it is closed, partially extracted, low-definition or deliberately empty, and a declared blank counts as legitimate content, not as a gap to disguise. The declared-omission rule: you may skip `territorio.md`, `arquitectura.md` or `visual.md`, but you must say so in `guia.md`, which the included example (Sole) demonstrates by omitting those three files. `verificacion.md` is a test suite any AI can run, not just a promise of quality. It is also the only one of the four that is native in Spanish.

What it lacks splits into two categories, and the standard names them differently:

**Pending (v1.1 in preparation):** a dedicated file for role and day-to-day responsibilities (today Whittemore is stronger there). The "what I am NOT prioritizing" category in goals, with explicit tradeoffs (today Whittemore and Creed name it better). Under evaluation: an integrity seal on the exported file, consistent with the standard's verification principle (me.md installed that idea and it is correct).

**Excluded by design, not pending:** multi-agent governance and per-section permissions. The `.contexto/` model is one owner and their AI; per-seat, per-role permissions belong to team products, and Creed solves that thesis well, but it is a different thesis. It also has no automatic sync, no scoring service, no connector of its own: the standard is a neutral file convention with no infrastructure behind it; the tools that operate the format are a separate layer, each implementer's own. Installing it means copying `system-prompt.txt`: that minimal friction, with no account and no lock-in, is a decision of the format, not a shortcoming.

### personal context portfolio (Whittemore)

Has: `role-and-responsibilities.md` and `team-and-relationships.md` are, across the four formats, the richest and most dedicated files on those two dimensions. `goals-and-priorities.md` explicitly names "what I am NOT prioritizing right now", a category no other format requests with that literalness. Three complete, pre-written example personas (knowledge worker, executive, entrepreneur) as starting points. An entire directory, `wiring/`, dedicated to integrations (MCP resource, Claude Projects, an API layer, system prompt patterns, OpenClaw agents), more extensive as a technical guide than `instalacion.md` in `.contexto/`. Explicit MIT license, built to be forked without friction.

Lacks: no governance or permissions at all. No date or versioning mechanism, not even a suggested "last updated" field in the templates. No explicit precedence between colliding rules. `decision-log.md` asks for real examples but requires neither a date nor the operating rule they left behind; it is more informal than `logica.md`. No runnable verification or audit of the format itself. No notion of "field state" or declared omission: an empty or half-filled file has no standard way of saying so.

### Creed

Has, with a clear margin over the other three: real per-section permissions, with its own pure, testable logic module (`lib/creed-permissions.ts`), four levels (hidden, read-only, propose, direct) and three roles on the Company plan (owner, admin, member), including the rule that an agent can never exceed its user's permission. Active GitHub sync (`creed.md`, sync hash, sync state). AI-driven quality scoring of the file. Built-in MCP plus OAuth 2.1, with named flows for more than ten agents (Claude Code, Codex, Cursor, Devin, OpenClaw, among others) and its own terminal client. Two sections with no equivalent in any other format: **Routines** (daily or weekly rhythms the AI must respect when planning) and **Health** (health, diet, accessibility).

Lacks: nothing resembling dated case law; it excludes it by design, with the agent contract listing "task-level trivia" and single-conversation notes as content that must never be proposed. No field states in the `.contexto/` sense (closed, partial, declared blank). No runnable verification or public audit of the format. No "who this is not for" or market-territory section; that makes sense for a personal rather than brand format, but it is a real absence next to `audiencias.md`. And, in its hosted form, it is a product with billing and paid plans, not a neutral, free file convention like `.contexto/` or Whittemore's repository.

### me.md

What is verifiable: a rapid-answer card model with measured, communicated progression (first signal at 5 answers, useful export at 40, strong context at 100, deep profile at 200, out of 247 total cards). A SHA-256 seal on the exported file; no other format offers a way to verify the file has not been altered. Explicit control of sensitivity and of what gets included when exporting or sharing. A category of its own, "Developer cards" (40+ technical questions: test-driven development bias, monorepo preference, agent autonomy, evaluation discipline), off by default, with no equivalent in the other three. It is, by far, the format most designed for mass adoption with minimal entry friction.

What it lacks, or cannot be verified: no published section schema. Its own FAQ says the file format ("Pack v1") and the card schema "may open up later if AGENTS.md-style portability gains adoption"; today it is closed. No auditable public repository; one was actively searched for and none was found. No public evidence of how it covers role, relationships, goals, history or per-section permissions: this map does not claim it lacks them, it states they are not verifiable from outside. No documented continuous-sync mechanism like Creed's.

## 3. Migration notes

### From personal context portfolio to `.contexto/`

`identity.md` maps directly to `identidad.md`, but you must add the real origin case (the specific moment the work became your own): `.contexto/` does not accept self-definition without a case, and `identity.md` is written as a summary, not as a scene. `communication-style.md` gets rewritten as `formas.md` by adding "like this / not like this" pairs with actually quoted phrases, not abstract style descriptions. `team-and-relationships.md` compresses into `audiencias.md`; per-person structure is lost unless you manually replicate the "what I need from them" and "what they need from me" fields. `decision-log.md` splits between `logica.md` (the rule and its precedence) and `evidencia.md` (what is claimable); every decision needs a date and an explicit operating rule that `decision-log.md` does not require.

Reverse path: `logica.md` and `evidencia.md` merge into a single `decision-log.md` when migrating to this format, losing the separation between "rule with precedence" and "verifiable case" that `.contexto/` keeps in two distinct files.

### From Creed to `.contexto/`

Identity, Work and Preferences spread across `identidad.md`, `arquitectura.md` (or directly into `guia.md` if the profile is simple) and `formas.md`; you must add cases and dates, because Creed's contract expressly prohibits the task-level detail that `.contexto/` demands as proof that something is real content. Goals pours into `identidad.md`, "current moment" block; Creed's "what DOES count as a goal" examples are lost unless rewritten as case law with their origin case. Constraints migrates directly to `restricciones.md`, but each rule must be classified as current, laboratory, horizon or history, a distinction Creed does not make. The per-section permission model (hidden, read-only, propose, direct) has no destination in `.contexto/`: multi-agent governance is excluded by design (one owner, their AI). If a use case needs per-agent, per-section permissions, Creed is today the right format for that.

Reverse path: `identidad.md`, `formas.md` and `restricciones.md` flatten into Creed's fixed sections (Identity, Preferences, Constraints), losing the dated case law with derived rules, because Creed's contract excludes precisely that kind of narrative content.

### From me.md to `.contexto/`

With what is verifiable today, only the "Quick Load" and "Communication" content can be migrated with confidence: it maps directly to `formas.md`, because it already arrives written as style rules with examples, close to the "like this / not like this" format `.contexto/` asks for. The "boundaries" cards, if answered, would migrate to `restricciones.md`. The rest (full identity, role, goals, relationships, history) cannot be mapped responsibly without access to the full schema of the 200+ cards: better to declare the gap, as the "honest states" principle of `.contexto/` itself demands, than to invent a destination for it.

Reverse path: it does not apply the same way. me.md is not an open standard for hand-written files; it is a closed product with its own card questionnaire. The only transferable move is using an already written `formas.md` and `restricciones.md` as prepared answers to speed up the questionnaire, if you want to generate a me.md anyway.

## 4. Sources

All four sources read on 2026-07-27. Anything not listed here was not read for this map.

**`.contexto/`**, repository `github.com/f0nchi/contexto-estandar`, branch `main`, 0 stars at reading time:
- `README.md` (the twelve-file table, the seven principles, installation, versioning)
- `auditoria.md`
- `instalacion.md`
- `system-prompt.txt`
- `ejemplo/guia.md`, `ejemplo/identidad.md`, `ejemplo/formas.md`, `ejemplo/restricciones.md`, `ejemplo/evidencia.md`, `ejemplo/logica.md`, `ejemplo/verificacion.md` (the complete Sole example)
- `plantillas/identidad.md`, `plantillas/audiencias.md`, `plantillas/feedback.md`, `plantillas/territorio.md`, `plantillas/visual.md`
- Full listing (names, not contents) of `ejemplo/` and `plantillas/` via `gh api repos/f0nchi/contexto-estandar/contents/...`

**personal context portfolio**, repository `github.com/nlwhittemore/personal-context-portfolio`, branch `main`, 447 stars at reading time:
- `README.md`
- `GETTING-STARTED.md`
- `templates/identity.md`, `templates/decision-log.md`, `templates/preferences-and-constraints.md`, `templates/team-and-relationships.md`, `templates/goals-and-priorities.md`
- `wiring/mcp-resource.md`
- Full listing (names, not contents) of `templates/`, `examples/knowledge-worker/`, `examples/` and `wiring/` via `gh api`. The contents of `interview-protocol/agent-system-prompt.md` (17 KB) and of the files inside `examples/` were not read, only their names

**Creed**, repository `github.com/connorhpbrn/creed`, branch `main`, 149 stars at reading time:
- `README.md`
- `AGENTS.md`
- `CHANGELOG.md`
- `lib/creed-permissions.ts` (full contents, the permissions module)
- `lib/creed-data.ts` (partial read: the definition of the ten sections with title and description, around lines 1027 to 1164; and the comment on the onboarding "core seed spine", around lines 736 to 745, within a 102 KB, 2588-line file not read in full)
- Root, `lib/`, `packages/` and `supabase/` listings via `gh api`

**me.md**, `getmemd.com` (Aprex):
- `https://getmemd.com` (home, read twice with different prompts: general structure, and navigation / example sections)
- `https://getmemd.com/build`
- `https://getmemd.com/faq`
- `https://getmemd.com/docs` returned 404, it does not exist
- Web search for a public repository ("getmemd.com me.md Aprex github repository format spec"): no relevant results, no repository found
- Everything that appears in the table as "not publicly verifiable" and is not cited above is exactly that: no public source was found to confirm it, and nothing was assumed by analogy with the other three formats
