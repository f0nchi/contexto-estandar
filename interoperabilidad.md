# Mapa de interoperabilidad: formatos de contexto e identidad para IA

> Parte del estándar [.contexto/](README.md). Segunda edición. Compara los formatos vivos que codifican identidad o contexto para que una IA los opere. Primera edición: 2026-07-27, cuatro formatos de contexto personal. Esta edición: 2026-08-14, con la familia de estándares de identidad de marca y la capa institucional que aparecieron en el medio. English version: [interoperabilidad.en.md](interoperabilidad.en.md).

El mapa cubre la categoría entera: qué resuelve cada formato, dónde `.contexto/` es más débil que los otros, y dónde los otros son más débiles entre sí. Cuando una fuente no se pudo verificar en detalle, el documento lo dice en vez de completar el hueco por analogía.

Las ausencias de cada formato se nombran en dos categorías distintas, porque son cosas distintas: **pendiente**, cuando el formato reconoce el hueco y está en camino de cubrirlo, y **excluido por diseño**, cuando la ausencia es una decisión de tesis con su razón declarada. Esta distinción aplica el principio de estados honestos de `.contexto/` al estándar mismo.

## Qué cambió desde la primera edición

En tres semanas el terreno pasó de una familia a tres.

Nació una familia entera de estándares de identidad de marca legible por agentes: el Brand Context Protocol de Encoded Brands, `brand.md`, `brandbook.md`, `brandkit.md`, y varios más que se listan abajo. Ninguno existía en el mapa de julio.

Apareció una capa institucional por encima de todos: el Open Knowledge Format de Google Cloud, que estandariza bundles de conocimiento en markdown con frontmatter, y AGENTS.md, ahora bajo la Agentic AI Foundation de la Linux Foundation.

Y de los cuatro formatos originales, dos se movieron y dos no: Creed sigue con desarrollo diario, el portfolio de Whittemore no tiene un solo commit desde el 26 de marzo aunque siguió acumulando estrellas.

## 1. El terreno en tres capas

Los formatos no compiten todos entre sí. Responden preguntas distintas y conviene separarlos antes de compararlos.

**Contexto de un sujeto persona.** Qué necesita saber una IA para trabajar con alguien: `.contexto/` en su modo persona, personal context portfolio, Creed y me.md.

**Identidad de una marca.** Qué necesita saber una IA para escribir, diseñar o hablar en nombre de una marca: `.contexto/` en su modo marca, Brand Context Protocol, `brand.md`, `brandbook.md`, `brandkit.md`, y en el borde `brand.yml`, `DESIGN.md` y `brandspec`, que resuelven la capa visual y de tokens.

**Conocimiento e instrucciones de una organización.** Qué sabe una organización y cómo se opera su código: Open Knowledge Format y AGENTS.md. Codifican materia y procedimiento, y se combinan con cualquiera de las dos capas anteriores.

`.contexto/` atraviesa las dos primeras capas con la misma estructura: su unidad es el sujeto que decide, y una persona y una marca son dos tipos de sujeto.

## 2. Tabla de equivalencias: sujeto persona

| Dimensión | `.contexto/` | personal context portfolio | Creed | me.md |
|---|---|---|---|---|
| **Identidad** | `identidad.md`: por qué existe el trabajo, qué mundo empuja, qué no debe perder. En personas suma "momento vigente" | `identity.md`: una página, el archivo mínimo si un agente solo puede leer uno | Sección **Identity** (fija): rol, rasgos estables, defaults que siguen a la persona | No verificable como sección propia; el ejemplo público muestra "Quick Load", con función parecida |
| **Rol / trabajo** | `rol.md` (v1.1): qué hace realmente contra lo que dice el puesto, la semana típica, con quién, qué decide, qué delega | `role-and-responsibilities.md`: cómo son las semanas en la práctica | Sección **Work** (fija): profesión, herramientas, métodos, colaboradores | No verificable públicamente |
| **Forma de decidir** | `logica.md`: jurisprudencia con fecha, regla derivada y precedencia explícita entre reglas que chocan | `decision-log.md`: cómo decide, dos o tres decisiones reales con su razonamiento | Parcial, sección **Beliefs** (opcional). Sin casos ni precedencia | Mencionado como categoría capturada, sin sección ni ejemplo visible |
| **Voz / estilo** | `formas.md`: síntesis, muestras así sí / así no con frases citadas, prohibiciones con su reemplazo, tono por contexto | `communication-style.md` | Sección **Preferences** (fija): tono, longitud, profundidad, formato | Parcialmente confirmado: sección "Communication" más tarjetas de escritura |
| **Relaciones** | `audiencias.md`, con nota lateral para personas sin mercado propio | `team-and-relationships.md`: campos por persona | Sección **People** (opcional), con ejemplos por persona | No verificable públicamente |
| **Objetivos** | `identidad.md` para el horizonte y `rol.md` para las prioridades vigentes, con la categoría "qué NO estoy priorizando" y el tradeoff de cada renuncia (v1.1) | `goals-and-priorities.md`: incluye tradeoffs y qué NO está priorizando | Sección **Goals** (fija), con ejemplos de qué cuenta y qué no | No verificable públicamente |
| **Restricciones** | `restricciones.md`: qué nunca haría, condiciones operativas, estados de promesa | `preferences-and-constraints.md`: reglas duras, restricciones personales | Sección **Constraints** (opcional): límites y temas que piden permiso | Mencionado como "boundaries", sin sección confirmada |
| **Historial / casos** | El más fuerte de los cuatro: `logica.md` más `evidencia.md` más `verificacion.md` | `decision-log.md`, bloque "Recent Decisions", sin fecha obligatoria ni regla derivada | Excluido por diseño: el contrato del agente descarta la nota de una sola conversación | No verificable; el modelo es de tarjetas, no de casos narrados |
| **Permisos / gobernanza** | Excluido por diseño: un dueño y su IA. Integridad resuelta en v1.1 con `SHA256SUMS` documentado | No cubierto | El más fuerte: cuatro niveles por sección, tres roles en el plan Company | Parcial: control de qué se comparte al exportar y sello SHA-256 |
| **Actualización** | `feedback.md` más versionado del estándar. Proceso manual | Sin mecanismo formal | El más automatizado: propuestas continuas de agentes, aprobación del dueño, sync con GitHub | Cuestionario progresivo, formato "Pack v1" todavía cerrado |
| **Movimiento del proyecto** | Última publicación 2026-07-27. 0 estrellas | Sin commits desde 2026-03-26. 454 estrellas, 305 forks | Desarrollo diario, último push 2026-08-14. 166 estrellas | Producto en v0.1, sin repositorio público |

## 3. Tabla de equivalencias: identidad de marca

| Dimensión | `.contexto/` | Brand Context Protocol | brand.md | brandbook.md |
|---|---|---|---|---|
| **Raíz** | `guia.md`: orden de lectura, reglas de operación, omisiones declaradas | `/.well-known/brand.md`: identidad, posicionamiento y registro de archivos hija | Archivo único con frontmatter (`name`, `tagline`, `version`, `language`, `specVersion`, `type`, `architecture`) | `BRANDBOOK.md` como índice de archivos temáticos |
| **Estrategia** | `identidad.md` más `territorio.md` más `arquitectura.md` | Posicionamiento en la raíz, valores en `values.md` | Capa **Strategy** obligatoria: overview, audience, positioning, personality, references y anti-references, promise, guardrails | Archivos de audiencia y contexto |
| **Voz** | `formas.md` | `voice.md` más `voice/anti-ai.md` para patrones de lenguaje generado | Capa **Voice**: identity, taglines, manifesto, message pillars, phrases, vocabulary, tonal rules | Archivo de voz |
| **Visual** | `visual.md`, con la regla de declarar la ausencia si no hay sistema | `visual.md` más extensiones opcionales (`tokens.json`, `tokens.css`, `DESIGN.md`) | Capa **Visual**: logo, core colors, typefaces, imagery, art direction | Archivo de assets |
| **Límites** | `restricciones.md`, con estados de promesa | `boundaries.md`: hard nos categóricos y soft nos con su condición | `guardrails` dentro de Strategy, con herencia que endurece y nunca debilita | Archivo de gobernanza |
| **Afirmaciones** | `evidencia.md`: afirmable, no afirmable, promesas permitidas | `claims.md`: claim, evidence, `proof_status` (approved, requires_caveat, forbidden, expired, aspirational, unknown), `valid_from` y `valid_until` | **Claims** en Governance: solo afirmaciones aprobadas por un humano o con prueba citada | Reglas ancla numeradas |
| **Cómo te describe un tercero** | `representacion.md` (v1.1): descripciones aprobadas en tres largos, con qué se confunde, qué nunca decir, comparaciones, trampas de encuadre | `representation.md`: descripciones aprobadas por longitud, con qué no confundir la marca, qué nunca decir, contra quién compara de verdad | No cubierto | No cubierto |
| **Descubrimiento** | Parcial: publica `representacion.md` en una ubicación conocida, enlazado y en datos estructurados, y declara que la ubicación conocida todavía no tiene consumidores. El resto de la carpeta queda privado a propósito | Resuelto: URL bien conocida en el dominio, más registro hosteado que firma los archivos y los sirve por MCP | Herencia por directorios dentro de un proyecto | No verificado en detalle |
| **Precedencia** | Entre reglas que chocan, por contenido y con su condición | Entre archivos, por jerarquía: campaña, producto, audiencia, locale, hija por defecto, raíz | Entre padre e hijo: los guardrails se fusionan, el hijo endurece | Referencias cruzadas entre secciones |
| **Estado y frescura** | Estados honestos por campo, incluido el vacío declarado, más frontmatter de procedencia y caducidad por archivo (v1.1) | Tres niveles de conformidad, `last_updated` por archivo, fechas de validez en claims | `specVersion` como puerta de validación, `version` entero incremental | Versionado tipo software |
| **Verificación** | `verificacion.md`: casos corribles por cualquier IA, con la respuesta esperada y la regla que la justifica. Más `auditoria.md`, un prompt que audita la carpeta contra los principios | Conformidad técnica: URI accesible, markdown y YAML válidos, hijas alcanzables | Validación contra la versión de spec declarada | No verificado en detalle |
| **Aprendizaje** | `feedback.md`: cada corrección del dueño con fecha, regla y ejemplo | No cubierto en la spec leída | No cubierto | No verificado en detalle |
| **Licencia y modelo** | CC BY 4.0, convención sin infraestructura | CC BY 4.0 la spec, MIT el código de referencia, con registro comercial por suscripción | MIT | CC BY 4.0 la spec, MIT el código |

En el borde de esta familia hay tres formatos más que resuelven la capa visual y de tokens antes que la identidad completa: `brand.yml`, `DESIGN.md` (de Google Stitch) y `brandspec`. Se los nombra porque aparecen en el paisaje de la categoría; no se leyeron en detalle para esta edición y no se afirma nada sobre su contenido.

## 4. La dimensión que ningún formato cubre

De los doce formatos revisados para esta edición, ninguno codifica hacia dónde mira el sujeto.

Todos resuelven la expresión: cómo suena, cómo se ve, qué puede afirmar, qué límites tiene, cómo debe describirlo un tercero. Ninguno resuelve la atención: qué universos observa, por dónde le entra el mundo, con qué lente lee un hecho nuevo y qué hace con lo que ve.

La consecuencia es estructural y se puede enunciar con precisión: cuando todos los archivos de una carpeta describen al sujeto, la única materia disponible para producir es el sujeto mismo. Una identidad codificada sin atención puede sostener el tono indefinidamente y solo puede hablar de sí.

La implementación de referencia de `.contexto/` corre `mirada.md` desde el 2026-08-13, con universos de atención derivados de los documentos lentos, fuentes de mundo declaradas, una lente de preguntas que ordena la lectura de cualquier hallazgo, y las señales que obligarían a revisar la propia tesis. Su entrada al estándar publicado está prevista para la v1.1. Hasta que eso pase, la fila de esta dimensión está vacía para los doce, incluido este.

## 5. Dos distinciones que parecen la misma cosa

**Validar formato y verificar comportamiento.** El Brand Context Protocol declara conformidad cuando el archivo está en la URI correcta, el markdown y el YAML son válidos y las hijas son alcanzables. `verificacion.md` de `.contexto/` corre situaciones y compara la respuesta contra la esperada, con la regla que la justifica. La primera comprueba que el envase esté bien armado; la segunda, que la identidad esté siendo operada. Un archivo puede ser perfectamente conforme y producir salidas que traicionan al sujeto.

Con la misma honestidad: la suite de `.contexto/` verifica fidelidad a lo declarado, con casos escritos en la propia carpeta. Verificar juicio, con casos retenidos fuera de la carpeta y comparación a ciegas, es una segunda forma que ningún formato de la categoría implementa todavía, este incluido.

**Precedencia entre archivos y precedencia entre reglas.** BCP resuelve qué archivo gana cuando dos aplican: una hija de campaña pisa a una de producto, que pisa a la raíz. `.contexto/` resuelve qué regla gana cuando dos principios del sujeto chocan, con su condición explícita, y admite registrar una tensión sin resolver cuando el dueño sostiene las dos posiciones. Son problemas distintos: uno es de resolución de alcance, el otro es de conflicto de valores.

## 6. Lo que cada formato tiene que los otros no

### `.contexto/`

Tiene: nueve principios explícitos y auditables, con un prompt de auditoría corrible. Jurisprudencia con caso, fecha y regla derivada, la dimensión más fuerte de toda la categoría. Precedencia entre reglas en conflicto, incluida la posibilidad de sostener una tensión sin promediarla. La regla de estados honestos, donde el vacío declarado es contenido legítimo. La regla de omisión declarada, que el ejemplo de Sole demuestra omitiendo tres archivos. Una suite de verificación de comportamiento. Un archivo que crece con las correcciones del dueño. Y es el único nativo en español de los doce, y el único que usa la misma estructura para una persona y para una marca.

**Resuelto en v1.1 (2026-08-14):** `mirada.md` para la atención, `rol.md` con la categoría "qué NO estoy priorizando" y sus tradeoffs, `representacion.md` para la tercera persona, y frontmatter de procedencia y frescura por archivo, compatible con el Open Knowledge Format, para que un derivado declare de dónde sale y cuándo caduca.

**Pendiente:** herencia entre marca madre, producto y submarca. Verificación de juicio con casos retenidos, que ningún formato de la categoría tiene. Y descubrimiento completo: se publica el material de tercera persona en una ubicación conocida, y el resto de la carpeta sigue viajando en mano, que es una decisión de privacidad antes que un hueco.

**Excluido por diseño:** gobernanza multiagente y permisos por sección, que pertenecen a productos para equipos y que Creed resuelve bien. Infraestructura propia: sincronización automática, scoring vía servicio o conector, porque el estándar es una convención de archivos neutral y las herramientas que lo operan son otra capa, de cada implementador.

### Brand Context Protocol (Encoded Brands)

Tiene, y con distancia sobre el resto de la familia: descubrimiento resuelto por URL bien conocida, de modo que un agente de un tercero puede leer la marca sin que nadie le pase nada. Un registro hosteado que firma los archivos y los sirve por MCP. Tres niveles de conformidad declarados. Precedencia jerárquica entre archivos por campaña, producto, audiencia y locale. `proof_status` con seis valores y fechas de validez en cada afirmación, con una política explícita de entidades nombradas. Un archivo dedicado a patrones de lenguaje generado por IA, con tipo, patrón, razón y ejemplo. Y `representation.md`, sin equivalente en ningún otro formato leído.

No tiene: casos con fecha ni jurisprudencia. Verificación de comportamiento. Aprendizaje acumulado por corrección del dueño. Una noción de estado del campo fuera de las afirmaciones. Y la spec pública iba por v0.7 mientras el archivo de la propia empresa ya declaraba v0.8, así que conviene leer las dos al integrar.

### brand.md (Caio Pizzol)

Tiene: la formulación más limpia de herencia entre marca madre, producto y submarca, con la regla de que un hijo puede endurecer un guardrail y nunca debilitarlo, y de que los compromisos de accesibilidad se fusionan siempre hacia arriba. `specVersion` como puerta de validación, con comportamiento definido para el archivo que no la declara. References y anti-references como campo obligatorio de estrategia. Licencia MIT y un solo archivo, la entrada más liviana de la familia.

No tiene: casos, fechas, jurisprudencia, verificación corrible, estados de completitud por campo, ni capa de representación. Declara los idiomas que soporta y el español no está entre ellos.

### personal context portfolio (Whittemore)

Tiene: los archivos más ricos de la categoría en rol y en relaciones, y la formulación más explícita de "qué NO estoy priorizando". Tres personas de ejemplo completas. Un directorio entero dedicado a integraciones. Licencia MIT.

No tiene: gobernanza, fechas, versionado, precedencia, verificación ni estados de campo. Y no recibe un commit desde el 26 de marzo, aunque sigue siendo el más adoptado por lejos, con 454 estrellas y 305 forks.

### Creed

Tiene: permisos reales por sección con su módulo de lógica testeable, sincronización activa con GitHub, scoring de calidad del archivo, conexión MCP con OAuth y flujos para más de diez agentes. Dos secciones sin equivalente en ningún otro formato: Routines y Health. Es el proyecto con desarrollo más activo de todos los revisados.

No tiene: jurisprudencia ni casos con fecha, excluidos por diseño. Estados de campo. Verificación corrible. Territorio o "para quién no es". Y en su forma hosteada es un producto con planes pagos.

### me.md

Lo verificable: progresión medible y comunicada por cantidad de tarjetas respondidas, un sello SHA-256 sobre el archivo exportado, control de sensibilidad al compartir, y una categoría propia de tarjetas técnicas apagada por defecto. La entrada más liviana de toda la categoría.

No tiene, o no se pudo verificar: esquema de secciones publicado, repositorio auditable, ni evidencia pública de cómo cubre rol, relaciones, objetivos o historial. No se afirma que no los tenga; se afirma que no es verificable desde afuera.

### Open Knowledge Format y AGENTS.md

Están en otra capa y conviene no compararlos de frente. OKF estandariza bundles de conocimiento con frontmatter que responde tres preguntas que ningún formato de identidad se hacía: de dónde salió esto (`sources`), quién lo produjo y quién lo confirmó (`generated`, `verified`), y si sigue vigente (`status`, `stale_after`). AGENTS.md estandariza instrucciones de proyecto para agentes de código y está adoptado por más de sesenta mil repositorios.

Ninguno de los dos codifica sujeto. La lectura útil es de encastre: un bundle de conocimiento no dice quién habla, y una carpeta de identidad no dice qué sabe la organización. Un sujeto completo va a necesitar las dos cosas, y expresar los estados de `.contexto/` en frontmatter compatible con OKF es el camino más corto para que las herramientas del ecosistema puedan leer una carpeta de identidad sin trabajo de integración.

## 7. Notas de migración

### Desde personal context portfolio hacia `.contexto/`

`identity.md` pasa directo a `identidad.md`, pero hay que sumarle el caso real de origen: `.contexto/` no acepta autodefinición sin caso, y `identity.md` está escrito como resumen, no como escena. `communication-style.md` se reescribe como `formas.md` agregando pares así sí / así no con frases citadas de verdad. `team-and-relationships.md` se comprime dentro de `audiencias.md`; se pierde estructura por persona salvo que se repliquen a mano los campos. `decision-log.md` se reparte entre `logica.md` y `evidencia.md`; cada decisión necesita una fecha y una regla operativa explícita que `decision-log.md` no exige.

Camino inverso: `logica.md` y `evidencia.md` se funden en un único `decision-log.md`, y se pierde la separación entre regla con precedencia y caso verificable.

### Desde Creed hacia `.contexto/`

Identity, Work y Preferences se reparten entre `identidad.md`, `arquitectura.md` y `formas.md`; hay que sumarles casos y fechas, porque el contrato de Creed prohíbe el detalle de tarea puntual que `.contexto/` exige como prueba. Goals se vuelca en `identidad.md`. Constraints migra directo a `restricciones.md`, clasificando cada regla en vigente, laboratorio, horizonte o historia. El modelo de permisos por sección no tiene destino: la gobernanza multiagente está excluida por diseño. Si un caso necesita permisos por agente y por sección, Creed es hoy el formato correcto.

Camino inverso: `identidad.md`, `formas.md` y `restricciones.md` se aplanan dentro de las secciones fijas de Creed, perdiendo la jurisprudencia con fecha y regla derivada.

### Desde me.md hacia `.contexto/`

Con lo verificable hoy, solo se puede migrar con confianza "Quick Load" y "Communication", que pasan a `formas.md`. Las tarjetas de boundaries migrarían a `restricciones.md`. El resto no se puede mapear de forma responsable sin acceso al esquema completo: mejor declarar el hueco que inventarle un destino.

### Desde Brand Context Protocol hacia `.contexto/`

`voice.md` pasa a `formas.md`, y `voice/anti-ai.md` entra como bloque de prohibiciones dentro del mismo archivo, conservando la tipificación por clase de patrón, que es más fina que la de `.contexto/`. `values.md` se reparte: las reglas de decisión van a `logica.md` y hay que agregarles el caso de origen y la fecha, que BCP no pide; las collision rules ya son precedencia y migran casi literales. `boundaries.md` va a `restricciones.md`, y los soft nos con condición encajan directo en el formato de condición operativa. `claims.md` va a `evidencia.md`, mapeando `proof_status` a los estados de promesa: approved a vigente, aspirational a horizonte, requires_caveat a insumo parcial. `visual.md` va a `visual.md`. `representation.md` no tiene destino hoy: es la capa de tercera persona que `.contexto/` todavía no cubre, y conviene conservar el archivo aparte hasta que la tenga.

Camino inverso: `logica.md` pierde sus casos y sus fechas al aplanarse en collision rules, y `verificacion.md` y `feedback.md` no tienen destino en BCP. A cambio se gana descubrimiento y firma, que `.contexto/` no tiene.

## 8. Fuentes

Fecha de lectura de esta edición: 2026-08-14. La edición anterior leyó los cuatro formatos personales el 2026-07-27 y sus fuentes siguen listadas abajo. Todo lo que no está acá no fue leído para este mapa.

**Brand Context Protocol / Encoded Brands** (leído el 2026-08-14):
- Especificación v0.7 completa en `brandcontextprotocol.dev/spec/v0.7/`
- `encodedbrands.ai/.well-known/brand.md` (archivo raíz real, que declara `bcp_version` 0.8 y `last_updated` 2026-08-05)
- Archivos hija reales: `voice.md`, `voice/anti-ai.md`, `values.md`, `boundaries.md`, `claims.md`, `representation.md`
- `encodedbrands.ai` (home, modelo comercial y planes)
- Metadatos del repositorio `github.com/Brand-Context-Protocol/spec` vía `gh api`: organización creada 2026-05-04, último push 2026-08-10, 1 estrella
- No se leyeron: `visual.md`, `commerce.md`, ni las extensiones opcionales (`manifest.json`, `tokens.json`)

**brand.md** (leído el 2026-08-14):
- `spec/brand-md.md` completo, versión 0.3.0, en `github.com/caiopizzol/brand.md`
- Metadatos del repositorio vía `gh api`: creado 2026-03-13, último push 2026-08-05, 22 estrellas, 4 forks, licencia MIT
- Perfil público del autor y `caiopizzol.com`

**brandbook.md** (leído el 2026-08-14):
- `brandbook.md/` (home: estructura de archivos, licencias, estado draft 0.1)
- `brandbook.md/landscape/` (su propia comparación de ocho estándares de marca)
- Metadatos vía búsqueda de repositorios: organización `brandbook-md`, creada 2026-07-16, 0 estrellas
- No se leyó la especificación archivo por archivo

**brandkit.md** (leído el 2026-08-14):
- `README.md` del repositorio `github.com/360vier/brandkit.md`, v0.1.0-draft
- Metadatos vía `gh api`: creado 2026-03-13, último push 2026-03-14, 1 estrella, licencia MIT

**Open Knowledge Format** (leído el 2026-08-14):
- `okf/SPEC.md` v0.2 completo en `github.com/GoogleCloudPlatform/knowledge-catalog`
- Anuncio en el blog de Google Cloud
- Cobertura secundaria para las fechas de v0.1 (2026-06-12) y v0.2 (2026-07-25)

**AGENTS.md** (leído el 2026-08-14): cobertura secundaria únicamente, para su estado institucional y su adopción declarada. No se leyó la especificación.

**Estado de los cuatro formatos personales al 2026-08-14**, verificado vía `gh api`: personal context portfolio 454 estrellas, 305 forks, último push 2026-03-26; Creed 166 estrellas, último push 2026-08-14; `.contexto/` 0 estrellas, último push 2026-07-27. Contenido de me.md releído en `getmemd.com`.

**Fuentes de la primera edición (2026-07-27)**, todas conservadas: `README.md`, `auditoria.md`, `instalacion.md`, `system-prompt.txt`, el ejemplo completo y cinco plantillas de `.contexto/`; `README.md`, `GETTING-STARTED.md`, cinco plantillas y `wiring/mcp-resource.md` del portfolio de Whittemore; `README.md`, `AGENTS.md`, `CHANGELOG.md`, `lib/creed-permissions.ts` completo y `lib/creed-data.ts` parcial de Creed; home, `/build` y `/faq` de me.md, con `/docs` inexistente y sin repositorio público encontrado.

**No verificado en esta edición:** `brand.yml`, `DESIGN.md` y `brandspec`, nombrados en la sección 3 sin afirmaciones sobre su contenido. Las otras dos iniciativas que usan el nombre Brand Context Protocol, de Aryabhatta Labs y de Wild, que aparecen en el paisaje de brandbook.md y no se leyeron. El changelog actual de Creed, cuyo archivo público remite a un módulo interno del repositorio que no se abrió.
