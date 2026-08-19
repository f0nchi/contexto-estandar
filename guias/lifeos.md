# Tu carpeta .contexto/ dentro de un LifeOS

> Guía de interoperabilidad · 2026-08-18 · Parte del estándar [.contexto/](../README.md)
> LifeOS es el sistema operativo de vida open source de Daniel Miessler (github.com/danielmiessler/LifeOS). Esta guía no está afiliada al proyecto: mapea cómo una carpeta `.contexto/` alimenta su capa de identidad, para que las dos comunidades se aprovechen.

## Por qué se tocan

LifeOS resuelve qué puede hacer un sistema personal con IA: skills, agentes, trabajos programados, memoria. Su capa de identidad (TELOS: misión, creencias, metas, proyectos, estilo de escritura) la llena cada instalador a mano. `.contexto/` resuelve exactamente esa capa: la identidad extraída de casos reales, con verificación corrible. Una carpeta bien construida es el mejor insumo para llenar un TELOS; un LifeOS es uno de los mejores lugares donde una carpeta puede trabajar.

## El mapeo, archivo por archivo

| `.contexto/` | En LifeOS | Nota |
|---|---|---|
| `identidad.md` | Los archivos de misión y creencias de TELOS | El porqué y las convicciones viajan casi directo. |
| `formas.md` | `WRITINGSTYLE` y `RHETORICALSTYLE` | Las muestras de así sí / así no valen más que cualquier descripción de estilo. |
| `logica.md` y `restricciones.md` | `STRATEGIES` | Las reglas con caso de origen se vuelven estrategias con fundamento; los límites, restricciones explícitas. |
| `rol.md` y el momento vigente de `identidad.md` | `GOALS` y proyectos | Los frentes abiertos y lo que NO se está priorizando, con su tradeoff. |
| `audiencias.md` | Contexto de proyectos y relaciones | Perfiles con caso vivido, no categorías. |
| `mirada.md` | Sin equivalente | LifeOS tiene memoria (Cortex); la atención codificada (universos, lente, señales contra la propia tesis) es aporte de `.contexto/`. |
| `verificacion.md` | Sin equivalente | La suite corrible de identidad no existe en LifeOS: corré los casos contra tu instalación y comprobá que responde como vos. |
| `feedback.md` | Pariente de la curación de Cortex | Las correcciones fechadas pueden alimentar las notas que Cortex promueve o vence. |

## Cómo se usa en la práctica

1. Construí o conseguí tu carpeta `.contexto/` (a mano con las [plantillas](../plantillas/), o extraída en una sesión).
2. Copiala dentro de tu instalación de LifeOS y volcá el mapeo de arriba en tus archivos TELOS, citando la carpeta como fuente.
3. Conservá la carpeta como fuente única: cuando cambie, regenerá lo mapeado. El estándar trae `SHA256SUMS` para saber si tu copia sigue íntegra.
4. Corré `verificacion.md` contra tu LifeOS: si responde tus casos como vos, la identidad viajó bien.

## Qué no mapea, a propósito

Los dos sistemas resuelven capas distintas y esta guía no intenta fusionarlos: LifeOS es infraestructura de ejecución con vocabulario propio y ritmo alto de releases; `.contexto/` es una convención de archivos neutral. La carpeta no depende de LifeOS para nada, y LifeOS funciona sin carpeta. Juntos, el sistema sabe hacer y además sabe quién es.
