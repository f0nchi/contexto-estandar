# Your .contexto/ folder inside a LifeOS

> Interoperability guide · 2026-08-18 · Part of the [.contexto/ standard](../README.en.md)
> LifeOS is Daniel Miessler's open source life operating system (github.com/danielmiessler/LifeOS). This guide is not affiliated with the project: it maps how a `.contexto/` folder feeds its identity layer, so both communities benefit.

## Why they meet

LifeOS solves what a personal AI system can do: skills, agents, scheduled jobs, memory. Its context layer (TELOS: mission, beliefs, goals, projects, writing style) is filled by hand by each installer. `.contexto/` contributes a portable base of materials, capabilities, and instructions, with runnable checks. A well-built folder is a useful input for TELOS; LifeOS is one place where that folder can activate work.

## The mapping, file by file

| `.contexto/` | In LifeOS | Note |
|---|---|---|
| `identidad.md` | TELOS mission and beliefs files | The why and the convictions travel almost directly. |
| `formas.md` | `WRITINGSTYLE` and `RHETORICALSTYLE` | Real yes/no samples beat any style description. |
| `logica.md` and `restricciones.md` | `STRATEGIES` | Rules with their originating case become grounded strategies; limits become explicit constraints. |
| `rol.md` plus the current moment in `identidad.md` | `GOALS` and projects | Open fronts and what is deliberately NOT being prioritized, with its tradeoff. |
| `audiencias.md` | Project and relationship context | Profiles built from lived cases, not categories. |
| `mirada.md` | No equivalent | LifeOS has memory (Cortex); codified attention (universes, the reading lens, signals against your own thesis) is a `.contexto/` contribution. |
| `verificacion.md` | No equivalent | Runnable checks for facts, formats, and operating conditions do not exist in LifeOS: run the cases against your install and inspect the concrete result. |
| `feedback.md` | Cousin of Cortex curation | Dated corrections can feed the notes Cortex promotes or expires. |

## In practice

1. Build or get your `.contexto/` folder (by hand with the [templates](../plantillas/), or extracted in a session).
2. Copy it into your LifeOS install and pour the mapping above into your TELOS files, citing the folder as source.
3. Keep the folder as the single source: when it changes, regenerate what you mapped. The standard ships `SHA256SUMS` so you know your copy is intact.
4. Run `verificacion.md` against your LifeOS: check facts, formats, and operating conditions in one concrete application.

## What deliberately does not map

The two systems solve different layers and this guide does not try to merge them: LifeOS is execution infrastructure with its own vocabulary and a fast release pace; `.contexto/` is a neutral file convention. The folder does not depend on LifeOS at all, and LifeOS works without a folder. Together, the system knows how to act and also knows who it is.
