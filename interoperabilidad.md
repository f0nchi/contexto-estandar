# Mapa de interoperabilidad: archivos de contexto personal para IA

> Parte del estándar [.contexto/](README.md). Compara los cuatro formatos vivos que codifican identidad o contexto personal para que una IA los opere: `.contexto/`, personal context portfolio, Creed y me.md. Fecha de lectura de las cuatro fuentes: 2026-07-27. English version: [interoperabilidad.en.md](interoperabilidad.en.md).

Este mapa no es un folleto de `.contexto/`. Es un mapa de la categoría: incluye dónde `.contexto/` es más débil que los otros tres, y dónde los otros tres son más débiles entre sí. Cuando una fuente no se pudo verificar en detalle, el documento lo dice en vez de completar el hueco por analogía.

Las ausencias de cada formato se nombran en dos categorías distintas, porque son cosas distintas: **pendiente** (el formato lo reconoce como hueco y está en camino) y **excluido por diseño** (una decisión de tesis, no una carencia). Esta distinción aplica el principio de estados honestos de `.contexto/` al estándar mismo.

## Los cuatro formatos, en una línea

- **`.contexto/`** (Ideas Aumentadas, f0nchi): convención abierta en español, doce archivos de texto plano (once núcleo más `feedback.md`), siete principios auditables, con plantillas y un ejemplo completo. Repositorio: `github.com/f0nchi/contexto-estandar`.
- **personal context portfolio** (Nathaniel Whittemore): diez archivos markdown en inglés, cada uno con un protocolo de entrevista embebido para que un asistente de IA lo redacte con el dueño. Licencia MIT. Repositorio: `github.com/nlwhittemore/personal-context-portfolio`, 447 estrellas.
- **Creed** (connorhpbrn): producto SaaS (Next.js más Supabase), un archivo `creed.md` por persona con diez secciones (cinco fijas, cinco opcionales) y permisos de escritura por sección para cada agente conectado. Repositorio: `github.com/connorhpbrn/creed`, 149 estrellas.
- **me.md** (Aprex, Noruega, `getmemd.com`): producto de código cerrado, sin repositorio público conocido (se buscó y no apareció uno). Cuestionario de tarjetas de opción múltiple que compila un README personal exportable. Estructura verificada solo de forma parcial: ver nota en la sección 1 y en las fuentes.

## 1. Tabla de equivalencias

| Dimensión | `.contexto/` | personal context portfolio | Creed | me.md |
|---|---|---|---|---|
| **Identidad** | `identidad.md`: por qué existe el trabajo, qué mundo empuja, qué no debe perder. En personas suma "momento vigente" | `identity.md`: una página, el archivo mínimo si un agente solo puede leer uno | Sección **Identity** (fija): rol, rasgos estables, defaults que siguen a la persona a todos lados | No verificable como sección propia. El ejemplo público muestra "Quick Load", con función parecida, sin confirmar que sea el equivalente formal |
| **Rol / trabajo** | Pendiente (entra en v1.1 como archivo propio de rol y operación semanal). Hoy `identidad.md` roza el porqué del trabajo, no la semana | `role-and-responsibilities.md`: cómo son las semanas en la práctica, no lo que dice el puesto formal | Sección **Work** (fija): profesión, herramientas, métodos, colaboradores recurrentes | No verificable públicamente |
| **Forma de decidir** | `logica.md`: jurisprudencia con fecha, regla derivada y precedencia explícita cuando dos reglas chocan | `decision-log.md`: cómo decide, qué necesita antes de decidir, dos o tres decisiones reales con el razonamiento, cómo maneja la incertidumbre | Parcial, sección **Beliefs** (opcional): valores y principios que cambian cómo la IA debe razonar. Sin casos ni precedencia | Mencionado como categoría capturada ("decision style") en la home del producto, sin sección ni ejemplo visible |
| **Voz / estilo** | `formas.md`: síntesis, muestras así sí / así no con frases citadas, prohibiciones con su reemplazo, tono por contexto | `communication-style.md` | Sección **Preferences** (fija): tono, longitud, profundidad, formato de respuesta | Parcialmente confirmado: sección "Communication" en el ejemplo público más tarjetas de escritura ("preferiría sonar un poco brusco antes que sobrepulido") |
| **Relaciones** | `audiencias.md`, con nota lateral para personas sin mercado propio. Reutiliza la estructura de audiencia de mercado; sin campos por persona | `team-and-relationships.md`: campos por persona (rol, cómo interactúan, qué necesita cada uno del otro) | Sección **People** (opcional), con ejemplos concretos por persona en el propio contrato del agente | No verificable públicamente |
| **Objetivos** | Parcial, dentro de `identidad.md`, bloque "momento vigente": frentes abiertos, horizonte a un año. La categoría explícita "qué NO estoy priorizando" es pendiente: entra en v1.1 | `goals-and-priorities.md`: incluye cómo resuelve tradeoffs y qué NO está priorizando | Sección **Goals** (fija), con ejemplos explícitos de qué cuenta y qué no cuenta como objetivo | No verificable públicamente |
| **Restricciones** | `restricciones.md`: qué nunca haría, condiciones operativas, estados de promesa (vigente, laboratorio, horizonte, historia) | `preferences-and-constraints.md`: reglas duras, lo que odia, restricciones personales | Sección **Constraints** (opcional): límites que la IA no debe cruzar, temas que piden permiso explícito | Mencionado como categoría capturada ("boundaries"), sin sección confirmada |
| **Historial / casos** | El más fuerte de los cuatro en esta dimensión: `logica.md` (jurisprudencia con fecha) más `evidencia.md` (afirmable / no afirmable) más `verificacion.md` (casos corribles por cualquier IA) | `decision-log.md`, bloque "Recent Decisions": dos o tres ejemplos reales, sin fecha obligatoria ni regla derivada explícita | Explícitamente afuera del modelo: el contrato del agente excluye por diseño "task-level trivia" y notas de una sola conversación | No verificable. Probablemente no aplica: el modelo es de tarjetas de opción, no de casos narrados con fecha |
| **Permisos / gobernanza** | Excluido por diseño: el modelo es un dueño y su IA, sin asientos ni niveles de acceso (ver sección 2). En evaluación para v1.1: sello de integridad del archivo exportado | No cubierto. Ningún archivo ni guía de `wiring/` define permisos o aprobación de cambios | El más fuerte con diferencia: `lib/creed-permissions.ts`, cuatro niveles por sección (hidden, read-only, propose, direct), tres roles en el plan Company (owner, admin, member) | Parcial: sin permisos por sección, pero con control de qué se comparte al exportar (nivel de sensibilidad, inclusión por toggle) y sello SHA-256 de integridad del archivo |
| **Actualización** | `feedback.md` (fecha, regla aprendida, ejemplo; proceso manual) más versionado del estándar mismo (v1.0, changelog con fecha y porqué) | Sin mecanismo formal. Un solo principio declarado: "actualizá regularmente" | El más automatizado: agentes proponen ediciones de forma continua, el dueño aprueba, sincronización bidireccional con GitHub, scoring de calidad del archivo vía IA | Cuestionario progresivo (primera señal a las 5 tarjetas, export útil a las 40, perfil profundo a las 200), producto en v0.1, formato "Pack v1" todavía cerrado |

## 2. Lo que cada formato tiene que los otros no

### `.contexto/`

Tiene: siete principios explícitos y auditables, con un prompt de auditoría corrible (`auditoria.md`) que cualquier IA puede correr contra la propia carpeta. Precedencia explícita cuando dos reglas chocan. La regla de "estados honestos": cada campo declara si está cerrado, con extracción parcial, con baja definición o vacío a propósito, y el vacío declarado cuenta como contenido legítimo, no como hueco a disimular. La regla de omisión declarada: se puede no tener `territorio.md`, `arquitectura.md` o `visual.md`, pero hay que decirlo en `guia.md`, algo que el propio ejemplo de Sole demuestra al omitir esos tres archivos. `verificacion.md` es una suite de tests corribles por cualquier IA, no solo una promesa de calidad. Es también el único de los cuatro nativo en español.

Lo que no tiene se divide en dos categorías, y el estándar las nombra distinto:

**Pendiente (v1.1 en preparación):** archivo dedicado a rol y responsabilidades del día a día (hoy Whittemore es más fuerte ahí). La categoría "qué NO estoy priorizando" en objetivos, con tradeoffs explícitos (hoy Whittemore y Creed la nombran mejor). En evaluación: un sello de integridad sobre el archivo exportado, coherente con el principio de verificación del estándar (la idea la instaló me.md y es correcta).

**Excluido por diseño, no pendiente:** gobernanza multiagente y permisos por sección. El modelo de `.contexto/` es un dueño y su IA; los permisos por asiento y por rol pertenecen a productos para equipos, y Creed resuelve bien esa tesis, que es otra. Tampoco tiene sincronización automática, scoring vía servicio ni conector propio: el estándar es una convención de archivos neutral, sin infraestructura detrás; las herramientas que operan el formato son otra capa, de cada implementador. Instalarlo es copiar `system-prompt.txt`: esa fricción mínima, sin cuenta y sin lock-in, es una decisión del formato, no una carencia.

### personal context portfolio (Whittemore)

Tiene: `role-and-responsibilities.md` y `team-and-relationships.md` son, de los cuatro formatos, los más ricos y dedicados en esas dos dimensiones. `goals-and-priorities.md` nombra de forma explícita "qué NO estoy priorizando ahora mismo", una categoría que ningún otro de los tres formatos pide con esa literalidad. Tres personas de ejemplo completas y ya redactadas (knowledge worker, executive, entrepreneur) como punto de partida. Un directorio entero, `wiring/`, dedicado a integraciones (recurso MCP, Claude Projects, capa de API, patrones de system prompt, agentes OpenClaw), más extenso como guía técnica que `instalacion.md` de `.contexto/`. Licencia MIT explícita, pensado para bifurcarse sin fricción.

No tiene: cero gobernanza o permisos. Cero mecanismo de fecha o versionado, ni siquiera un campo de "última actualización" sugerido en los templates. Cero precedencia explícita entre reglas que chocan. `decision-log.md` pide ejemplos reales pero no exige fecha ni la regla operativa que dejaron, es más informal que `logica.md`. No hay verificación corrible ni auditoría del propio formato. No hay noción de "estado del campo" ni de omisión declarada: un archivo vacío o a medio llenar no tiene forma estándar de decirlo.

### Creed

Tiene, con diferencia clara sobre los otros tres: permisos reales por sección, con su propio módulo de lógica pura y testeable (`lib/creed-permissions.ts`), cuatro niveles (hidden, read-only, propose, direct) y tres roles para el plan Company (owner, admin, member), incluida la regla de que un agente nunca puede exceder el permiso de su usuario. Sincronización activa con GitHub (`creed.md`, hash de sincronización, estado de sync). Scoring de calidad del archivo vía IA. Conexión MCP más OAuth 2.1 de fábrica, con flujos nombrados para más de diez agentes (Claude Code, Codex, Cursor, Devin, OpenClaw, entre otros) y un cliente de terminal propio. Dos secciones sin equivalente en ningún otro de los tres formatos: **Routines** (ritmos diarios o semanales que la IA debe respetar al planificar) y **Health** (salud, alimentación, accesibilidad).

No tiene: nada de jurisprudencia o casos con fecha, lo excluye por diseño, el propio contrato del agente lista "task-level trivia" y notas de una sola conversación como contenido que nunca debe proponerse. Nada de "estado del campo" tipo `.contexto/` (cerrado, parcial, vacío declarado). Nada de verificación corrible ni auditoría pública del formato. No tiene una sección de "para quién no es" o de territorio de mercado, tiene sentido porque es personal y no de marca, pero es una ausencia real frente a `audiencias.md`. Y es, en su forma hosteada, un producto con billing y planes pagos, no una convención de archivos neutral y libre como `.contexto/` o el repositorio de Whittemore.

### me.md

Lo verificable: un modelo de tarjetas de respuesta rápida con progresión medible y comunicada (primera señal a las 5 respuestas, export útil a las 40, contexto fuerte a las 100, perfil profundo a las 200, sobre un total de 247 tarjetas). Un sello SHA-256 sobre el archivo exportado, ningún otro de los cuatro formatos ofrece una forma de verificar que el archivo no fue alterado. Control explícito de sensibilidad y de qué se incluye al exportar o compartir. Una categoría propia, "Developer cards" (más de 40 preguntas técnicas: sesgo a test-driven development, preferencia de monorepo, autonomía del agente, disciplina de evaluación), apagada por defecto, sin equivalente en los otros tres. Es, de lejos, el más pensado para consumo masivo con fricción mínima de entrada.

No tiene, o no se pudo verificar: ningún esquema de secciones publicado. El propio FAQ dice que el formato de archivo ("Pack v1") y el esquema de tarjetas "pueden abrirse más adelante si la portabilidad estilo AGENTS.md gana adopción", hoy es cerrado. Sin repositorio público auditable, se buscó de forma activa y no apareció ninguno. Sin evidencia pública de cómo cubre rol, relaciones, objetivos, historial o permisos por sección: no se afirma que no los tenga, se afirma que no es verificable desde afuera. Sin mecanismo de sincronización continua documentado como el de Creed.

## 3. Notas de migración

### Desde personal context portfolio hacia `.contexto/`

`identity.md` pasa directo a `identidad.md`, pero hay que sumarle el caso real de origen (el momento puntual en que el trabajo se volvió propio): `.contexto/` no acepta autodefinición sin caso, y `identity.md` está escrito como resumen, no como escena. `communication-style.md` se reescribe como `formas.md` agregando pares así sí / así no con frases citadas de verdad, no descripciones de estilo en abstracto. `team-and-relationships.md` se comprime dentro de `audiencias.md`; se pierde estructura por persona salvo que se repliquen a mano los campos "qué necesito de él" y "qué necesita de mí". `decision-log.md` se reparte entre `logica.md` (la regla y su precedencia) y `evidencia.md` (qué es afirmable); cada decisión necesita una fecha y una regla operativa explícita que `decision-log.md` no exige.

Camino inverso: `logica.md` y `evidencia.md` de `.contexto/` se funden en un único `decision-log.md` al migrar hacia este formato, y se pierde la separación entre "regla con precedencia" y "caso verificable" que `.contexto/` mantiene en dos archivos distintos.

### Desde Creed hacia `.contexto/`

Identity, Work y Preferences se reparten entre `identidad.md`, `arquitectura.md` (o directo en `guia.md` si el perfil es simple) y `formas.md`; hay que sumarles casos y fechas, porque el contrato de Creed prohíbe expresamente el detalle de tarea puntual que `.contexto/` exige como prueba de que algo es contenido real. Goals se vuelca en `identidad.md`, bloque "momento vigente"; se pierden los ejemplos de "qué SÍ cuenta como objetivo" de Creed salvo que se reescriban como jurisprudencia con su caso de origen. Constraints migra directo a `restricciones.md`, pero hay que clasificar cada regla en vigente, laboratorio, horizonte o historia, algo que Creed no distingue. El modelo de permisos por sección (hidden, read-only, propose, direct) no tiene destino en `.contexto/`: la gobernanza multiagente está excluida por diseño (un dueño y su IA). Si un caso necesita permisos por agente y por sección, Creed es hoy el formato correcto para eso.

Camino inverso: `identidad.md`, `formas.md` y `restricciones.md` de `.contexto/` se aplanan dentro de las secciones fijas de Creed (Identity, Preferences, Constraints), perdiendo la jurisprudencia con fecha y regla derivada, porque el contrato de Creed excluye justamente ese tipo de contenido narrativo.

### Desde me.md hacia `.contexto/`

Con lo verificable hoy, solo se puede migrar con confianza el contenido de "Quick Load" y "Communication": pasa directo a `formas.md`, porque ya viene redactado como reglas de estilo con ejemplos, un formato cercano al así sí / así no que pide `.contexto/`. Las tarjetas de "boundaries", si el usuario las tiene respondidas, migrarían a `restricciones.md`. El resto (identidad completa, rol, objetivos, relaciones, historial) no se puede mapear de forma responsable sin acceso al esquema completo de las más de 200 tarjetas: mejor declarar el hueco, como pide el propio principio de "estados honestos" de `.contexto/`, que inventarle un destino.

Camino inverso: no aplica del mismo modo. me.md no es un estándar abierto para escribir archivos a mano, es un producto cerrado con su propio cuestionario de tarjetas. Lo único trasladable es usar `formas.md` y `restricciones.md` ya redactados como respuestas preparadas de antemano, para acelerar el cuestionario si de todos modos se quiere generar un me.md.

## 4. Fuentes

Fecha de lectura de las cuatro fuentes: 2026-07-27. Todo lo que no está listado acá no fue leído para este mapa.

**`.contexto/`**, repositorio `github.com/f0nchi/contexto-estandar`, rama `main`, 0 estrellas al momento de la lectura:
- `README.md` (tabla de los doce archivos, los siete principios, instalación, versionado)
- `auditoria.md`
- `instalacion.md`
- `system-prompt.txt`
- `ejemplo/guia.md`, `ejemplo/identidad.md`, `ejemplo/formas.md`, `ejemplo/restricciones.md`, `ejemplo/evidencia.md`, `ejemplo/logica.md`, `ejemplo/verificacion.md` (contenido completo del ejemplo de Sole)
- `plantillas/identidad.md`, `plantillas/audiencias.md`, `plantillas/feedback.md`, `plantillas/territorio.md`, `plantillas/visual.md`
- Listado completo (nombres, sin contenido) de `ejemplo/` y `plantillas/` vía `gh api repos/f0nchi/contexto-estandar/contents/...`

**personal context portfolio**, repositorio `github.com/nlwhittemore/personal-context-portfolio`, rama `main`, 447 estrellas al momento de la lectura:
- `README.md`
- `GETTING-STARTED.md`
- `templates/identity.md`, `templates/decision-log.md`, `templates/preferences-and-constraints.md`, `templates/team-and-relationships.md`, `templates/goals-and-priorities.md`
- `wiring/mcp-resource.md`
- Listado completo (nombres, sin contenido) de `templates/`, `examples/knowledge-worker/`, `examples/` y `wiring/` vía `gh api`. No se leyó el contenido de `interview-protocol/agent-system-prompt.md` (17 KB) ni de los archivos dentro de `examples/`, solo sus nombres

**Creed**, repositorio `github.com/connorhpbrn/creed`, rama `main`, 149 estrellas al momento de la lectura:
- `README.md`
- `AGENTS.md`
- `CHANGELOG.md`
- `lib/creed-permissions.ts` (contenido completo, el módulo de permisos)
- `lib/creed-data.ts` (lectura parcial: definición de las diez secciones con su título y descripción, líneas cercanas a 1027 a 1164; y el comentario sobre la "core seed spine" de onboarding, líneas cercanas a 736 a 745, sobre un archivo de 102 KB y 2588 líneas, no leído completo)
- Listado de la raíz, `lib/`, `packages/` y `supabase/` vía `gh api`

**me.md**, `getmemd.com` (Aprex):
- `https://getmemd.com` (home, leída dos veces con prompts distintos: estructura general y navegación / secciones de ejemplo)
- `https://getmemd.com/build`
- `https://getmemd.com/faq`
- `https://getmemd.com/docs` devolvió 404, no existe
- Búsqueda web de un repositorio público ("getmemd.com me.md Aprex github repository format spec"): sin resultados relevantes, no se encontró repositorio
- Todo lo que no aparece citado arriba y sí aparece en la tabla como "no verificable públicamente" es exactamente eso: no se encontró fuente pública que lo confirme, no se asumió por analogía con los otros tres formatos
