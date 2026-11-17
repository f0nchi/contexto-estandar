# The .contexto/ standard

**Version 2.1 · November 17, 2026 · Maintained by [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · CC BY 4.0**

An open structure, with Spanish filenames, for organizing a person's, brand's or team's context, materials and capabilities in text files that different AI tools can read and extend.

[Repository](https://github.com/f0nchi/contexto-estandar) · [Español](README.md)

## Purpose and scope

The folder provides a personal working base: who it belongs to, what they want to do, the materials available and the criteria that guide their work. Its guide points to the information relevant to each task. The files remain readable, editable and portable.

The standard defines the structure and the meaning of its parts. Each person chooses how to build and use it. [Trama](https://www.ideasaumentadas.com.ar/trama) is an open reference implementation by Ideas Aumentadas, distributed separately with its working method, introductory conversation and base skills. That conversation and its starting words are not requirements of this format.

## Structure

The folder can be named `contexto/` or `.contexto/`. Its entry point is `guia.md`, which identifies its owner and scope, available materials and capabilities, and incomplete sections.

```text
contexto/
├── guia.md
├── identidad.md
├── formas.md
└── tareas/
    └── capability-name/
        └── SKILL.md
```

This is one way to start, not a checklist that must be completed before working. Add documents when they serve the case and declare relevant omissions in the guide. Preserve the defined filenames so their purpose remains recognizable across folders.

| File | Purpose |
|---|---|
| `guia.md` | Owner, scope, index, state and references needed to use the base. |
| `identidad.md` | What they do, for whom, current work and what they want to be able to do. |
| `formas.md` | Writing and speaking, with real samples and personal criteria. |
| `tareas/<name>/SKILL.md` | One capability: audience, outcome, materials, instructions and references. |
| `casos.md` | Facts, data and cases with their provenance. |
| `identidad-visual.md` | Colors, typography, composition and visual resources. |
| `mirada.md` | References, sources and questions that guide attention and exploration. |
| `audiencias.md` | People or groups and the situations in which the work reaches them. |
| `territorio.md` | Topics, situations and questions to develop. |
| `arquitectura.md` | Creative directions connecting materials and potential applications. |
| `rol.md` | Responsibilities, actual working week, decisions and boundaries. |
| `con-quien-trabajo.md` | People or roles and the context of working relationships. |
| `representacion.md` | Approved information for others to describe the owner. |
| `logica.md` | Dated decisions, scope, reasoning and precedence. |
| `restricciones.md` | Relevant privacy, data, third-party and operational conditions. |
| `verificacion.md` | Facts or conditions to verify and where to verify them. |
| `feedback.md` | Observations awaiting interpretation or confirmation, when useful. |

Projects, outputs and histories can live alongside this folder. The guide locates relevant materials. The standard does not require particular names for those external folders, an interview, starting commands, a review schedule or a delegation sequence.

## Capabilities

Each capability has its own folder under `tareas/` and a `SKILL.md` with `name` and `description` frontmatter. Its body explains who it serves, what it can produce or enable, and the materials and instructions it uses. It may include a procedure, quality criteria with their scope, output format and references to previous applications. Distinguish proposed capabilities from tested ones and identify approved examples as such. Integrate changes into the relevant instruction, optionally keeping a short dated record.

The [template](plantillas/tareas/nombre-de-la-tarea/SKILL.md) provides an example structure. The capability catalog and procedures belong to each implementation. There is no required number of skills or requirement for a completed first application.

## Principles

1. **Potential comes first.** Context opens capabilities; experience and materials provide a starting point.
2. **Real materials, explicit directions.** Preserve the provenance of facts and identify proposals, including possibilities not yet developed.
3. **Honest states.** Distinguish incomplete, provisional and confirmed information without inventing missing facts.
4. **Dated, scoped criteria.** Preserve the work, person or situation a decision applies to, and its reasoning and original case when useful.
5. **Verifiable facts.** Relevant data has a source or a place to check its currency.
6. **Explicit precedence.** A new instruction supersedes an older one within the same scope; unresolved contradictions stay identified.
7. **A base for creation.** Materials and examples support new applications and are interpreted for each case.
8. **A personal perspective.** The owner's references and questions can guide observation and exploration.
9. **Distinct uses.** Working with the owner and describing them to others require appropriate materials and permissions.
10. **Room to grow.** Applications can expand materials, criteria and capabilities. Adopted decisions enter their proper place; unconfirmed observations retain that state.

These principles guide the structure. It can be developed in conversation, by hand or with different tools.

## State, provenance and scope

Plain Markdown can express dates, sources, state and scope. Template YAML metadata is optional; `status`, `stale_after` and other fields are not universal requirements. Skill frontmatter retains its own identification purpose.

An adopted instruction has one current home. Optional `feedback.md` can hold observations awaiting interpretation without duplicating every decision. An idea to explore is distinct from a work commitment.

When a base includes several clients or projects, identify each context's subject and indicate when to consult it. A client's preference retains that scope. Separate contexts and cross-references are allowed; their arrangement depends on the work.

## Extension and continuity

Add a file when it organizes material or a capability that existing documents cannot hold clearly. Explain its purpose and location in the guide. Extend an existing document when that is sufficient.

Older folders remain valid, including the historical filenames `evidencia.md` and `visual.md` when the guide identifies them. Version 2.0 working folders can keep their method; v2.1 recognizes that method as an implementation, rather than a format requirement.

A recoverable copy or version history helps preserve work during reorganization. Each implementation chooses its mechanism. Connections, automations and tool permissions are outside the format.

## Materials and ownership

This repository provides [templates](plantillas/), [Sole's fictional example](ejemplo/LEEME.md), [installation guidance](instalacion.md), an [optional entry instruction](system-prompt.txt), a [structural review](auditoria.md) and [decision history](decisiones.md). The dated [interoperability map](interoperabilidad.en.md) and [LifeOS guide](guias/lifeos.en.md) are supporting material, not requirements.

The specification, templates and example are available under [CC BY 4.0](LICENSE.md), with attribution to Ideas Aumentadas. Content added by an owner retains its ownership and privacy. The structure neither publishes files nor grants third-party access. Trama distributes its full open method and license separately; either can be used and adapted independently.

## Version history

Changes to the standard are recorded in this file, with their date.

- **v2.1 (2026-11-17).** Defines the standard as structure, principles and document meaning. The conversational method is distributed separately in Trama. Clarifies criterion scope, optional metadata, extensions and states. Existing folders remain valid. Earlier entries describe the scope of their respective versions.
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
