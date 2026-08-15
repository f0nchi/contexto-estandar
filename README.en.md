# The .contexto/ standard

**Version 1.1 · August 15, 2026 · Maintained by [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · CC BY 4.0**

An open convention for encoding the working intelligence of a person or a brand into a folder of plain text files that any AI can read and operate.

The standard is written in Spanish and its file names are Spanish. This is the English guide to it. Canonical repository: https://github.com/f0nchi/contexto-estandar · Standard page: https://www.ideasaumentadas.com.ar/estandar

## Why a folder of plain text

The intelligence of a job already exists: it lives in how you decide, in what you can claim, in what you would never do, in the reasoning behind every position you have taken. Written down in plain markdown, that intelligence passes three tests at once: any AI reads it natively, any human can open and edit it, and it is yours for good, portable across platforms, with no vendor lock-in.

This standard defines how to organize it so an AI does more than read it: so it can operate from it.

## The folder

A `.contexto/` folder has thirteen core files, one that grows with use, and one specific to encoding a person.

| File | What it encodes |
|---|---|
| `guia.md` | Guide. Entry point: what the folder is, reading order, operating rules, state of this version. |
| `identidad.md` | Identity. Why this work or this brand exists, what world it pushes for, what it must not lose. For people: the current moment as well. |
| `mirada.md` | Gaze. Where the subject looks: fields of attention, the lens it reads a new fact through, what feeds it, and what evidence would count against its own thesis. |
| `formas.md` | Forms. How it writes and speaks: synthesis, real samples of yes-like-this and not-like-this, prohibitions with their replacement, tone by context. |
| `territorio.md` | Territory. What it talks about, what it does not, where the border runs, levels of conversation. |
| `audiencias.md` | Audiences. Real profiles with a lived case, who it is not for. For people: working relationships. |
| `arquitectura.md` | Architecture. Pillars that hold the content up, structures that already worked. |
| `restricciones.md` | Constraints. What it would never do, operating conditions, promise states. |
| `logica.md` | Logic. Case law: real cases with date and rationale, rules, and what wins when two rules collide. |
| `evidencia.md` | Evidence. Verifiable cases, what can be claimed and what cannot yet, which promises are allowed. |
| `visual.md` | Visual. The visual system if one exists. If it does not, that is declared: no AI should invent one. |
| `representacion.md` | Representation. What an AI that does not work for the subject may say about them: approved descriptions, what it gets confused with, what never to say, framing traps. |
| `verificacion.md` | Verification. The identity's test suite: cases any AI can run. |
| `rol.md` | Role. People only: what the weeks actually look like, with whom, what they decide, what they delegate, and what they are NOT prioritizing, with the tradeoff. |
| `feedback.md` | Feedback. The file that grows with use: every correction from the owner, one line with date, rule and example. |

### Where to start

The folder is built in order, and the order matters because the first files hold up the ones that follow: `guia.md`, `identidad.md`, `formas.md`, `restricciones.md`, `logica.md` and `verificacion.md` complete the first full loop, covering the subject, how they write, their limits, how they decide, and how to check that an AI is operating them well. Then come `mirada.md`, `territorio.md`, `audiencias.md`, `arquitectura.md`, `evidencia.md`, `visual.md`, `representacion.md` and, for people, `rol.md`. `feedback.md` starts filling up from the first day of use.

A folder halfway through is a legitimate state and it is declared in `guia.md`. What is not legitimate is leaving out something the subject does have: omission is valid when the field does not apply, never to get there sooner.

### Admission criteria for new files

This standard grows carefully, and the bar for adding a file is this: it answers a question none of the existing files answer, it was born from a failure observed in use with its date and its case, the example can demonstrate it with real content, and its absence shows up in what the AI produces rather than only in the tidiness of the schema. A candidate that fails any of the four goes in as a section of an existing file, and most candidates are exactly that. Every evaluation is recorded in [decisiones.md](decisiones.md), including the negative ones: a standard that only shows what it accepted never reveals its bar.

Not every file applies to every case. A professional profile can omit territory, architecture and visual; a brand omits `rol.md`. The omission is declared in `guia.md`, never disguised.

## The principles

What makes a folder a `.contexto/` folder are these nine rules, ahead of the file names.

**1. Real cases, literal phrases.** Every entry comes from something that happened, with the owner's own words quoted verbatim. A self-definition that would fit anyone in the same field is not content yet.

**2. Honest states.** Every field declares its state: closed, partially extracted, low definition, or declared empty. On a field that is not closed the AI does not invent: it asks or flags the gap. A declared emptiness is legitimate content ("this brand has no public cases yet; the AI claims method, not results").

**3. Case law with dates.** Decisions are recorded as cases: what happened, what rule it left, when. A rule without its originating case is worth less: the case is what lets an AI reason through situations nobody anticipated.

**4. Runnable verification.** The folder carries its own test suite: situation, expected response, what never, and the rule that justifies it. Any AI that has read the folder can run it, and the owner can check they are being operated with their own logic instead of improvisation.

**5. Explicit precedence.** When two rules collide, the folder says which one wins and under what condition. Without precedence the AI averages, and averaging is the quietest way to betray an identity.

**6. The folder is the lens, not the script.** The AI writes and decides from these documents without describing them, and without turning the limits, the method or the anti-examples into public content.

**7. Where it looks.** Identity includes its attention. When every file describes the subject, the only available material to produce from is the subject itself, and an encoded identity with no gaze can only talk about itself. `mirada.md` encodes what it observes, the lens it reads through, and what would change the owner's mind.

**8. First and third person kept apart.** The folder serves an AI writing and deciding as the owner, and it serves an outside agent describing them. Those are two different materials and they do not mix: what governs the owner's own writing lives across the whole folder, and what a third party may say lives only in `representacion.md`, limited to what the owner authorizes.

**9. Memory of corrections.** Every correction from the owner is proposed as a new line in `feedback.md`: date, rule learned, example. The identity accumulates case law through use.

## How it is installed

On chat platforms (ChatGPT, Claude, Gemini): a dedicated project or assistant, the folder loaded as knowledge files, and an instruction block telling the model to read `guia.md` first. In code editors and agents (Cursor, Claude Code): the folder at the project root, and one line in the agent's rules file: "Before working with me, read `.contexto/guia.md`."

## How it is published

The whole folder is private by default: `logica.md` and `restricciones.md` govern decisions and are not third-party material. The only file written for the outside is `representacion.md`, and for that one the standard recommends four moves, ordered by verifiable effect.

**Mirror the approved descriptions in your site's structured data.** This is the only path with real consumers today. In schema.org: `description` for the approved one, `disambiguatingDescription` for what you get confused with, plus `slogan`, `knowsAbout` and `subjectOf` pointing at the file.

**Publish the file at `/.well-known/representacion.md`** on your domain, using the prefix defined by [RFC 8615](https://www.rfc-editor.org/rfc/rfc8615.html).

**Link it from your HTML** with `<link rel="alternate" type="text/markdown" href="/.well-known/representacion.md">`, the mechanism the web has used to declare alternate representations of a resource for decades.

**Add it to your sitemap**, so the crawlers already walking your site find it.

The last three are a bet, and it is worth saying so plainly: as of August 2026 no major model provider states that it reads context files published on a domain. Public measurement of `llms.txt`, which has considerably more adoption than any identity format, recorded 408 hits across 500 million AI bot visits over ninety days. Publishing does not get you read; it gets there to be something worth reading when someone looks, and today whoever looks is usually a person handing your address to their assistant.

## How to build yours

The templates in `plantillas/` carry the structure of each file with its guidance inside, to fill in by hand. In `ejemplo/` there is Sole's complete folder, a sample professional profile that also demonstrates the declared-omission rule. And to use it from day one: `system-prompt.txt` (the block ready to paste into any AI), `instalacion.md` (how to load it into ChatGPT, Claude, Gemini and coding agents) and `auditoria.md` (a prompt for any AI to audit your folder against the nine principles and tell you what is missing).

The assisted path exists at [Ideas Aumentadas](https://www.ideasaumentadas.com.ar): a first context file free in the browser, and extraction sessions with an agent that works from real cases and delivers the full folder with its verification suite.

## How it relates to other formats

The category has several living formats. [interoperabilidad.en.md](interoperabilidad.en.md) is the full map: the three layers of the terrain, equivalence tables against the personal context portfolio, Creed, me.md, the Brand Context Protocol, brand.md and brandbook.md, what each format covers that the others do not, and migration notes in both directions. It includes what this standard is missing today and what it excludes on purpose, because the honest-states principle applies to the standard itself.

## Versioning

Changes to the standard are recorded in this file, with date and rationale.

- **v1.1 (2026-08-15).** The two decisions left open by the July map are closed. Integrity: `instalacion.md` documents how to generate and verify `SHA256SUMS`, and this repository publishes its own; cryptographic signing is declared out of scope. Publication: the standard recommends where and how to publish `representacion.md`, with the real effect of each path declared rather than promised.
- **v1.1 (2026-08-14).** `mirada.md` enters as a core file and attention as the seventh principle: an encoded identity with no gaze can only talk about itself. `rol.md` enters for the person mode, carrying the "what I am NOT prioritizing" category with its tradeoffs, until now the most frequently flagged gap in the format. Every file gains provenance and freshness frontmatter (`status`, `generated`, `stale_after`, and `sources` when the file is derived from another source), compatible with the Open Knowledge Format. `representacion.md` enters, and with it the separation of first and third person as the ninth principle: answers about a subject are already being given by assistants that are not theirs, and without this file they get assembled from whatever is around. `formas.md` classifies its prohibitions by class (word, structure, opening, closing), because structural ones slip through when everything is read at the same level. `identidad.md` adds what each conviction costs to hold, and `visual.md` adds where the tokens live and the rule that they travel inside the folder when it is handed over. Why: a derived file that fell behind its source gets operated exactly like a current one, with no way to notice, and the case that produced the rule happened inside this standard's own reference folder.
- **v1.0 (2026-07-20).** First public version: eleven core files plus `feedback.md`, seven principles, templates and example.
- **Expanded materials (2026-07-22).** The standard does not change; its materials are completed: Sole's example goes from three files to the whole folder (with the omissions declared in her `guia.md`, demonstrating that rule), and `system-prompt.txt`, `instalacion.md` and `auditoria.md` are added. Why: a format is learned through its example, and the example was one third done.
- **Interoperability map (2026-07-27).** The standard does not change; `interoperabilidad.md` is published (with an English version): equivalences with the other three living formats of the category, its own absences split into pending for v1.1 and excluded by design, and migration notes in both directions. Why: an open standard becomes trustworthy when it shows the full map, including where it loses.

## License and attribution

This standard is published under [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/): use it, adapt it and redistribute it, with attribution to Ideas Aumentadas. See `LICENSE.md`.

If the standard is useful to you, a star on [the repository](https://github.com/f0nchi/contexto-estandar) helps more people find it.
