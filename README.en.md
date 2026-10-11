# The .contexto/ standard

**Version 1.5 · October 11, 2026 · Maintained by [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · CC BY 4.0**

An open convention for organizing the context, materials, and capabilities of a person or brand in plain text files that any AI can read, use, and expand.

The standard is written in Spanish and its file names are Spanish. This is the English guide to it. Canonical repository: https://github.com/f0nchi/contexto-estandar · Standard page: https://www.ideasaumentadas.com.ar/estandar

## Why a folder of plain text

The context of a job already exists: it lives in what you do, the materials you use, the people you work with, and the possibilities you want to open. Written down in plain markdown, that context passes three tests at once: any AI reads it natively, any human can open and edit it, and it is yours for good, portable across platforms, with no vendor lock-in.

This standard defines how to organize it so an AI does more than read it: so it can operate from it.

## Getting started

Three files are enough for an AI to start creating with you: `guia.md`, `identidad.md` and `formas.md`. Copy their templates from `plantillas/`, fill them with real materials and your own words, load the folder with `system-prompt.txt`, and ask for one concrete first application. Then use it, expand a capability, or try something else. The rest of the folder grows through use.

## The folder

A `.contexto/` folder has thirteen core files, two specific to encoding a person, the tasks folder, and one optional file.

| File | What it encodes |
|---|---|
| `guia.md` | Guide. Entry point: what the folder is, reading order, operating rules, state of this version. |
| `identidad.md` | Identity. What it does today, for whom, with which materials, and which possibilities it wants to open. For people: the current moment as well. |
| `mirada.md` | Gaze. Where the subject looks: fields of attention, the lens it reads a new fact through, what feeds it, and what evidence would count against its own thesis. |
| `formas.md` | Forms. Resources for writing and speaking: real samples, rhythm, structures, words, and possibilities to explore. |
| `territorio.md` | Territory. Topics, scenes, and questions it can explore; routes into new conversations. |
| `audiencias.md` | Audiences. Real people and situations: what it can say, show, or offer them. |
| `arquitectura.md` | Architecture. Creation routes that can become content, campaigns, presentations, or other pieces. |
| `restricciones.md` | Constraints. Operating conditions, privacy, applicable rules, and factual safeguards. These do not define the folder's potential. |
| `logica.md` | Logic. Case law: real cases with date and rationale, rules, and what wins when two rules collide. |
| `casos.md` | Cases. Cases, data, and facts available as verifiable source material. |
| `identidad-visual.md` | Visual identity. Colors, typography, composition, alignment, logo use, assets, and references for visual creation. |
| `representacion.md` | Material another AI can use to describe the subject: ready-to-use descriptions, category and differences, factual precision, comparisons, and useful frames. |
| `verificacion.md` | Verification. Runnable checks for facts, formats, and operating conditions. |
| `rol.md` | Role. People only: what the weeks actually look like, with whom, what they decide, what they delegate, and what they are NOT prioritizing, with the tradeoff. |
| `con-quien-trabajo.md` | Who I work with. People only: the real people they work with and how they talk to each one. |
| `tareas/` | Capabilities. One folder per capability, each with its `SKILL.md`: what it enables, who it is for, which materials it uses, and a first application. The folder name stays stable for compatibility. |
| `feedback.md` | Feedback. Optional: a record of the criteria the owner wants to keep while using the folder, with date and case. |

### Where to start

The folder starts with a usable base: `guia.md`, `identidad.md`, `formas.md`, and at least one capability in `tareas/`. The capability can be written while producing the first real application. Then add `mirada.md`, `territorio.md`, `audiencias.md`, `arquitectura.md`, `casos.md`, `identidad-visual.md`, `logica.md`, `restricciones.md`, `verificacion.md`, `representacion.md`, and, for people, `rol.md` and `con-quien-trabajo.md`. Each file expands what the AI can do and adds material for new applications.

The base can grow in stages. `guia.md` names the materials available now and what can be added later; a first application lets you start working with what you already have.

### Admission criteria for new files

A new file makes sense when it opens a capability, gives materials a useful home, or addresses a need observed in use. Include a concrete application showing what it enables. When extending an existing file is enough, start there. Decisions about the format are recorded in [decisiones.md](decisiones.md); each person can extend their folder for the work they want to do.

Not every file applies to every case. A professional profile can omit territory, architecture and visual; a brand omits `rol.md`. The omission is declared in `guia.md`, never disguised.

## The principles

What makes a folder a `.contexto/` folder are these ten principles, ahead of the file names.

**1. Potential comes first.** The folder exists to open things a person or brand can do, say, use, or show with AI. Prior work is source material, not the boundary of what is possible.

**2. Real materials, explicit directions.** The base brings together writing, references, cases, assets, and possibilities the owner wants to explore. Quotes preserve their words, facts name their source, and proposals are presented as proposals. It can also guide work that has not been done yet.

**3. Honest states.** Every field declares its state: closed, partially extracted, low definition, or declared empty. On a field that is not closed the AI does not invent facts: it asks, proposes a labelled hypothesis, or flags the gap.

**4. Case law with dates.** Decisions are recorded as cases: what happened, what rule it left, when. A rule without its originating case is worth less: the case is what lets an AI reason through situations nobody anticipated.

**5. Runnable verification.** The folder carries cases that can verify facts, formats, and operating conditions. Each review leaves a clearer application and useful material for the next one.

**6. Explicit precedence.** When two instructions collide, the folder says which one wins and under what condition.

**7. The folder is the base, not the script.** The AI creates from these documents without reciting them or treating them as a ceiling. A first application puts the folder to work and opens what comes next.

**8. Where it looks.** Identity includes its attention. `mirada.md` encodes what it observes, the lens it reads through, and which new materials it can bring into the work.

**9. First and third person kept apart.** The folder serves the owner's own work and can provide factual material to an outside agent describing them. Those are two different uses and their materials do not mix.

**10. The folder expands through use.** Each application can add material, adjust an instruction, or open a capability. `feedback.md` can preserve what was learned with its date and case; the owner decides what moves into `formas.md`, `tareas/`, or `verificacion.md`.

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

The templates in `plantillas/` carry the structure of each file with its guidance inside, to fill in by hand. In `ejemplo/` there is Sole's complete folder, a sample professional profile that also demonstrates the declared-omission rule. And to use it from day one: `system-prompt.txt` (the block ready to paste into any AI), `instalacion.md` (how to load it into ChatGPT, Claude, Gemini and coding agents) and `auditoria.md` (a prompt for any AI to audit your folder against the ten principles and suggest which capability to use, expand, or explore next).

The assisted path exists at [Ideas Aumentadas](https://www.ideasaumentadas.com.ar): a first context file free in the browser, and sessions with an agent that organizes real materials, produces a first application, and delivers the full portable folder.

## How it relates to other formats

The category has several living formats. [interoperabilidad.en.md](interoperabilidad.en.md) is the full map: the three layers of the terrain, equivalence tables against the personal context portfolio, Creed, me.md, the Brand Context Protocol, brand.md and brandbook.md, what each format covers that the others do not, and migration notes in both directions. It includes what this standard is missing today and what it excludes on purpose, because the honest-states principle applies to the standard itself.

## Versioning

Changes to the standard are recorded in this file, with their date.

- **v1.5 (2026-10-11).** The folder is organized around operational potential: context and materials open capabilities to do, say, use, and show things with AI. `tareas/` keeps its name and schema for compatibility, while each entry becomes an expandable capability. The first application proves the base can be used; it is no longer a final fidelity verdict. Visual identity now explicitly covers composition, alignment, typography, logo use, resources, and references. Factual safeguards, privacy, and applicable rules remain intact without defining the product's center of gravity.
- **v1.4 (2026-10-01).** The standard adds `tareas/`: one folder per task, each with its `SKILL.md`, in the skills format. Person mode adds `con-quien-trabajo.md`. Two files take more direct names: `casos.md` (formerly `evidencia.md`) and `identidad-visual.md` (formerly `visual.md`); existing folders remain valid with the previous names. Sole's example includes a task.
- **v1.3 (2026-10-01).** The standard adds "Getting started": the three files a person begins with, how to load them and how they are kept current. The ninth principle describes how the folder is updated through use, and `feedback.md` becomes an optional record of the owner's criteria. `system-prompt.txt`, the `feedback.md` template and Sole's example follow.
- **v1.2 (2026-08-29).** The standard adds how a folder stays sharp while it is in use. Four practices enter as rules of existing files, none as a new file. In `formas.md`: samples are marked as light rather than mold, and the section of AI language patterns is now named the model's register, born nearly empty and filled through operation. In `mirada.md`: what comes in from outside passes through `formas.md` before it becomes text. In `feedback.md` and the ninth principle: the promotion cycle, from correction to prohibition to runnable case; Sole's example shows it. In `guia.md`: two operating rules, the owner's instructions steer without being recited in the output, and a batch is re-read as a whole before it ships. Why: a folder used every day needs to know how to stay sharp. The detail of each evaluation lives in [decisiones.md](decisiones.md).
- **v1.1 (2026-08-15).** The two decisions left open by the July map are closed. Integrity: `instalacion.md` documents how to generate and verify `SHA256SUMS`, and this repository publishes its own; cryptographic signing is declared out of scope. Publication: the standard recommends where and how to publish `representacion.md`, with the real effect of each path declared rather than promised.
- **v1.1 (2026-08-14).** `mirada.md` enters as a core file and attention as the seventh principle: an encoded identity with no gaze can only talk about itself. `rol.md` enters for the person mode, carrying the "what I am NOT prioritizing" category with its tradeoffs, until now the most frequently flagged gap in the format. Every file gains provenance and freshness frontmatter (`status`, `generated`, `stale_after`, and `sources` when the file is derived from another source), compatible with the Open Knowledge Format. `representacion.md` enters, and with it the separation of first and third person as the ninth principle: answers about a subject are already being given by assistants that are not theirs, and without this file they get assembled from whatever is around. `formas.md` classifies its prohibitions by class (word, structure, opening, closing), because structural ones slip through when everything is read at the same level. `identidad.md` adds what each conviction costs to hold, and `visual.md` adds where the tokens live and the rule that they travel inside the folder when it is handed over. Why: a derived file that fell behind its source gets operated exactly like a current one, with no way to notice, and the case that produced the rule happened inside this standard's own reference folder.
- **v1.0 (2026-07-20).** First public version: eleven core files plus `feedback.md`, seven principles, templates and example.
- **Expanded materials (2026-07-22).** The standard does not change; its materials are completed: Sole's example goes from three files to the whole folder (with the omissions declared in her `guia.md`, demonstrating that rule), and `system-prompt.txt`, `instalacion.md` and `auditoria.md` are added. Why: a format is learned through its example, and the example was one third done.
- **Interoperability map (2026-07-27).** The standard does not change; `interoperabilidad.md` is published (with an English version): equivalences with the other three living formats of the category, its own absences split into pending for v1.1 and excluded by design, and migration notes in both directions. Why: an open standard becomes trustworthy when it shows the full map, including where it loses.

## License and attribution

This standard is published under [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/): use it, adapt it and redistribute it, with attribution to Ideas Aumentadas. See `LICENSE.md`.

If the standard is useful to you, a star on [the repository](https://github.com/f0nchi/contexto-estandar) helps more people find it.
