# The .contexto/ standard

**Version 2.0 · November 10, 2026 · Maintained by [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · CC BY 4.0**

An open convention for organizing the context, materials, and capabilities of a person or brand in plain text files that any AI can read, use, and expand.

The standard is written in Spanish and its file names are Spanish. This is the English guide to it. Canonical repository: https://github.com/f0nchi/contexto-estandar · Standard page: https://www.ideasaumentadas.com.ar/estandar

## Why a folder of plain text

The context of a job already exists: it lives in what you do, the materials you use, the people you work with, and the possibilities you want to open. Written down in plain markdown, that context passes three tests at once: any AI reads it natively, any human can open and edit it, and it is yours for good, portable across platforms, with no vendor lock-in.

This standard defines how to organize it so an AI does more than read it: so it can operate from it.

## Getting started

The shortest way: download the working folder (`carpeta/` in this repository, or from [ideasaumentadas.com.ar/trama](https://www.ideasaumentadas.com.ar/trama)), open it with an AI app that works on the folders of your computer, and type «empecemos». The AI asks and writes the documents as you answer.

By hand: three files are enough for an AI to start creating with you: `guia.md`, `identidad.md` and `formas.md`. Copy their templates from `plantillas/`, fill them with real materials and your own words, load the folder with `system-prompt.txt`, and ask for one concrete first application. Then use it, expand a capability, or try something else. The rest of the folder grows through use.

## The folder

A `.contexto/` folder has nine material files, the capabilities folder, one file so another AI can describe the owner, two files for the person mode, and four optional safeguards.

**Material to create with**

| File | What it brings |
|---|---|
| `guia.md` | Guide. Entry point: what is in the folder, reading order, how it is used, and the state of this version. |
| `identidad.md` | Identity. What it does today, for whom, with which materials, and what it wants to be able to do. For people: the current moment as well. |
| `formas.md` | Forms. How it writes and speaks: complete real samples, rhythm, structures, and its own words. |
| `casos.md` | Cases. Cases, data, and facts available as material to create with. |
| `identidad-visual.md` | Visual identity. Colors, typography, composition, alignment, logo use, assets, and references for visual pieces. |
| `mirada.md` | References. What it follows, where it learns about it, and which sources and examples help its work. |
| `audiencias.md` | Audiences. Real people and situations: what it can say, show, or offer them. |
| `territorio.md` | Territory. Topics, scenes, and questions it can work on. |
| `arquitectura.md` | Architecture. Creation routes: structures and pillars that can become content, campaigns, presentations, or other pieces. |
| `tareas/` | Capabilities. One folder per capability, each with its `SKILL.md`: what it produces, who it is for, which materials and instructions it uses, and a first application when there is one. Standard skills format. |

**So another AI can describe the owner**

| File | What it brings |
|---|---|
| `representacion.md` | Approved descriptions, category and differences, dated facts, and useful frames to present the owner from the outside. |

**Person mode**

| File | What it brings |
|---|---|
| `rol.md` | Role. What the weeks actually look like, with whom, what they decide, what they delegate, and what they leave out, with its cost. |
| `con-quien-trabajo.md` | Who I work with. The real people they work with and how they talk to each one. |

**Safeguards, optional**

| File | What it brings |
|---|---|
| `restricciones.md` | Operating conditions: data, privacy, third parties, states of what is promised, applicable rules. One line per condition, with what to do. |
| `verificacion.md` | Checks on facts, formats, and conditions: prices, names, figures, dates, and delivery formats, with the place where each one is verified. |
| `logica.md` | Dated decisions: what happened, what stayed, when; and which instruction goes first when two collide. |
| `feedback.md` | A record of the criteria the owner keeps while using the folder, with date and case. |

### Where to start

The folder starts usable with `guia.md`, `identidad.md`, `formas.md`, and one capability in `tareas/`; the capability can be written while making the first piece. Then come `casos.md`, `identidad-visual.md`, `mirada.md`, `audiencias.md`, `territorio.md`, and `arquitectura.md`, as a task asks for them. `representacion.md` comes in when another AI has to describe the owner. The safeguards come in when a piece touches prices, data, third parties, or rules, and they stay short. In person mode, `rol.md` and `con-quien-trabajo.md` come in when the work needs them. Each file adds material for new pieces.

The base can grow in stages. `guia.md` names the materials available now and what can be added later; a first application lets you start working with what you already have.

### Admission criteria for new files

A new file makes sense when it opens a capability, gives materials a useful home, or addresses a need observed in use. Include a concrete application showing what it enables. When extending an existing file is enough, start there. Decisions about the format are recorded in [decisiones.md](decisiones.md); each person can extend their folder for the work they want to do.

Not every file applies to every case. A professional profile can omit territory, architecture and visual; a brand omits `rol.md`. The omission is declared in `guia.md`, never disguised.

## The working folder

Since v2.0 the standard also describes the folder the AI works in every day. The context folder sits inside it, visible, under the name `contexto/`, so the person can find it in their file explorer. In a code repository it can stay hidden as `.contexto/`.

```
my-folder/
├── AGENTS.md        how the AI works in this folder
├── CLAUDE.md        loads AGENTS.md and contexto/guia.md in Claude apps
├── LEEME.md         the explanation for the person
├── sesion.md        the conversation that builds the context
├── auditoria.md     the periodic review
├── pasos.md         the steps for handing more work to the AI
├── contexto/        the context folder: documents and tareas/
└── trabajo/         what the AI produces
    ├── registro.md  what is done and what is pending
    └── <matter>/    one folder per client or project, with its estado.md
```

| File | What it brings |
|---|---|
| `AGENTS.md` | The method: what the AI reads before working, how it works, what the person approves, and how each job is closed. It is the file agents read by convention. |
| `CLAUDE.md` | Two lines that load `AGENTS.md` and `contexto/guia.md` in Claude apps. |
| `LEEME.md` | Read me. The explanation for the person: how to start and what is in the folder. |
| `sesion.md` | Session. The conversation through which the AI builds the context: it asks, the person answers, and the AI writes the documents. |
| `auditoria.md` | Review. The periodic review: it tidies the folder, removes what went stale, and proposes what to add. |
| `pasos.md` | Steps. The steps through which a person hands more work to their AI, each with the signal that tells when to propose it. |
| `contexto/` | The context folder this standard defines. |
| `trabajo/` | Work. What the AI produces. `registro.md` keeps what is done and what is pending. Each client or project has its own folder with an `estado.md`: who takes part, what was agreed, what is done, and what is missing. |

### How work happens in it

Six rules. The full text is in `AGENTS.md`.

1. **Read first.** Before answering, the AI reads `contexto/guia.md`. If the request matches a capability, it reads its `SKILL.md`. If it belongs to a client or project with its own folder, it reads its `estado.md`.
2. **Work is saved.** Whatever the person will pick up again or reuse is saved to a file inside `trabajo/`.
3. **Each correction is written once, in its place.** How a task is done, in its skill. How the person writes, in `formas.md`. How they want to be helped and which permissions they gave, in `guia.md`. A new fact, in the document it belongs to. A decision that holds from then on, in `logica.md`, dated.
4. **Anything that leaves the folder is approved.** Before sending, publishing, paying, deleting, or changing anything outside the folder, the AI shows what it is about to do and waits for a yes. A standing permission is written in `guia.md` with the date and the person's own words.
5. **Each job is closed.** The AI updates the client or project state and the log, and tells the person what it wrote down.
6. **Three words.** «empecemos» (let's start) builds the context with `sesion.md`. «sumemos» (let's add) adds a capability or a document. «revisemos» (let's review) tidies the folder with `auditoria.md`.

`guia.md` declares the state of the folder: «sin empezar» (not started), «sesión a medio hacer» (session in progress) with the list of what is still untold, or complete, with the step of `pasos.md` the person is at.

The ready-to-use folder is in [`carpeta/`](carpeta/) in this repository. It is the same one [Trama](https://www.ideasaumentadas.com.ar/trama) delivers. It comes with eleven base skills in `contexto/tareas/`, for the most common tasks: they work from day one and adjust to the person through use.

A `.contexto/` folder on its own, loaded into a chat project or a repository, is still valid. The working folder is the complete form, for people using an app that reads and writes files on their computer.

## The principles

What makes a folder a `.contexto/` folder are these ten principles, ahead of the file names.

**1. Potential comes first.** The folder exists to open things a person or brand can do, say, use, or show with AI. Prior work is source material, not the boundary of what is possible.

**2. Real materials, explicit directions.** The base brings together writing, references, cases, assets, and possibilities the owner wants to explore. Quotes preserve their words, facts name their source, and proposals are presented as proposals. It can also guide work that has not been done yet.

**3. Honest states.** Every field declares its state: closed, partially extracted, low definition, or declared empty. On a field that is not closed the AI does not invent facts: it asks, proposes a labelled hypothesis, or flags the gap.

**4. The owner's decisions keep their date.** When the owner corrects a piece or sets a criterion, the folder keeps it as a case: what happened, what stayed, when. The next piece starts knowing that.

**5. Facts are checked before going out.** Prices, names, figures, dates, and delivery formats have a place where they are verified, and the folder says which one for each.

**6. When two instructions collide, the folder says which one goes first.** A newer criterion from the owner replaces the earlier one; a condition about data or third parties comes before a style preference.

**7. The folder is the base, not the script.** The AI creates from these documents without reciting them or treating them as a ceiling. A first application puts the folder to work and opens what comes next.

**8. Where it looks.** Identity includes its attention. `mirada.md` encodes what it observes, the lens it reads through, and which new materials it can bring into the work.

**9. First and third person kept apart.** The folder serves the owner's own work and can provide factual material to an outside agent describing them. Those are two different uses and their materials do not mix.

**10. The folder expands through use.** Each application can add material, adjust an instruction, or open a capability. `feedback.md` can preserve what was learned with its date and case; the owner decides what moves into `formas.md`, `tareas/`, or `verificacion.md`.

## How it is installed

With an app that works on the folders of your computer (the Claude desktop app in its Code tab, Codex, and agents that read `AGENTS.md`): open the app in the working folder. `AGENTS.md` and `CLAUDE.md` already tell the AI to read `contexto/guia.md` first. Where the app does not load those files on its own, the first line of the conversation is "read AGENTS.md and follow it".

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

The assisted path is [Trama](https://www.ideasaumentadas.com.ar/trama), by Ideas Aumentadas: the working folder of this standard, free, downloaded with its first documents already written from four questions. The ready-to-use folder is also in `carpeta/`.

## How it relates to other formats

The category has several living formats. [interoperabilidad.en.md](interoperabilidad.en.md) is the full map: the three layers of the terrain, equivalence tables against the personal context portfolio, Creed, me.md, the Brand Context Protocol, brand.md and brandbook.md, what each format covers that the others do not, and migration notes in both directions. It includes what this standard is missing today and what it excludes on purpose, because the honest-states principle applies to the standard itself.

## Versioning

Changes to the standard are recorded in this file, with their date.

- **v2.0 (2026-11-10).** A major version, because it changes what the standard describes: from the context folder to the whole working folder. The standard adds the working folder: the folder the AI works in every day, with `contexto/` inside, `trabajo/` for what gets produced, and the files that organize the method (`AGENTS.md`, `CLAUDE.md`, `sesion.md`, `auditoria.md`, `pasos.md`). Six rules are written down: what is read before working, where work is saved, where each correction goes, what is approved before leaving the folder, how a job is closed, and the three words that open each moment. The ready-to-use folder is published in `carpeta/` and is the one Trama delivers. Existing `.contexto/` folders remain valid with no changes. Why: AI apps moved to working on the folders of the computer, and well-written context does more when it comes with the place where the work is kept and with the way of working.
- **v1.6 (2026-10-12).** The folder is ordered by what an AI uses to create: nine material files and the capabilities folder, in the order a task asks for them. `restricciones.md`, `verificacion.md`, and `logica.md` accompany as optional safeguards, short and at the end, and principles 4, 5, and 6 are written from their use: dated decisions, facts that get checked, and which instruction goes first when two collide. This is the shape Trama has delivered since October 11 and the one the Ideas Aumentadas, Fonchi, and Orkos folders have. Why: a folder an AI creates with works best when the first thing it finds is the material and what it can do with it; the safeguards keep caring for facts and data, in their place.
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
