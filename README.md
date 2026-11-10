# El estándar .contexto/

**Versión 2.0 · 10 de noviembre de 2026 · Mantenido por [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · Licencia CC BY 4.0**

Una convención abierta, en español, para organizar el contexto, los materiales y las capacidades de una persona o una marca en archivos de texto plano que cualquier IA puede leer, usar y ampliar.

Repositorio canónico: https://github.com/f0nchi/contexto-estandar · Página del estándar: https://www.ideasaumentadas.com.ar/estandar · English: [README.en.md](README.en.md)

## Por qué una carpeta de texto plano

El contexto de un trabajo ya existe: está en lo que hacés, en tus materiales, en las personas con las que trabajás y en las posibilidades que querés abrir. Cuando queda escrito en markdown plano, pasa tres pruebas a la vez: cualquier IA lo lee nativamente, cualquier humano lo puede abrir y editar, y es tuyo para siempre, portable entre plataformas, sin lock-in de ningún proveedor.

Este estándar define cómo organizarla para que una IA no solo la lea: la opere.

## Para empezar

La manera más corta: bajá la carpeta de trabajo (`carpeta/` en este repositorio, o desde [ideasaumentadas.com.ar/trama](https://www.ideasaumentadas.com.ar/trama)), abrila con una app de IA que trabaje sobre las carpetas de tu computadora y escribí «empecemos». La IA pregunta y va escribiendo los documentos.

A mano: con tres archivos una IA ya puede empezar a crear con vos: `guia.md`, `identidad.md` y `formas.md`. Copiá sus plantillas de `plantillas/`, completalas con materiales reales y tus propias palabras, cargá la carpeta en tu IA con `system-prompt.txt` y pedile una primera aplicación concreta. Después podés usarla, ampliar una capacidad o probar otra cosa. El resto de la carpeta se suma con el uso.

## La carpeta

Una carpeta `.contexto/` tiene nueve archivos de material, la carpeta de capacidades, uno para que otra IA describa al dueño, dos propios del modo persona y cuatro resguardos opcionales.

**Material para crear**

| Archivo | Qué trae |
|---|---|
| `guia.md` | Punto de entrada: qué hay en la carpeta, en qué orden se lee, cómo se usa y el estado de la versión. |
| `identidad.md` | Qué hace hoy, para quién, con qué materiales y qué quiere poder hacer. Para personas: también el momento vigente. |
| `formas.md` | Cómo escribe y habla: textos reales completos, ritmo, estructuras y palabras propias. |
| `casos.md` | Casos, datos y hechos disponibles como material para crear. |
| `identidad-visual.md` | Colores, tipografías, composición, alineación, logos, recursos y referencias para crear piezas visuales. |
| `mirada.md` | Referencias: de qué se ocupa, por dónde se entera, qué fuentes y ejemplos le sirven para trabajar. |
| `audiencias.md` | Personas y situaciones reales: qué puede decirles, mostrarles u ofrecerles. |
| `territorio.md` | Temas, escenas y preguntas que puede trabajar. |
| `arquitectura.md` | Rutas de creación: estructuras y pilares que pueden convertirse en contenido, campañas, presentaciones o piezas. |
| `tareas/` | Una carpeta por capacidad, con su `SKILL.md`: qué produce, para quién, con qué materiales e instrucciones, y una primera aplicación cuando existe. Formato estándar de skills. |

**Para que otra IA lo describa**

| Archivo | Qué trae |
|---|---|
| `representacion.md` | Descripciones aprobadas, categoría y diferencias, datos con fecha y encuadres útiles para presentar al dueño desde afuera. |

**Modo persona**

| Archivo | Qué trae |
|---|---|
| `rol.md` | Cómo son las semanas de verdad, con quién, qué decide, qué delega y qué deja afuera con su costo. |
| `con-quien-trabajo.md` | Las personas reales con las que trabaja y cómo le habla a cada una. |

**Resguardos, opcionales**

| Archivo | Qué trae |
|---|---|
| `restricciones.md` | Condiciones operativas: datos, privacidad, terceros, estados de lo prometido, normas. Una línea por condición, con qué se hace. |
| `verificacion.md` | Comprobaciones de hechos, formatos y condiciones: precios, nombres, cifras, fechas y formatos de entrega, con el lugar donde se verifica cada uno. |
| `logica.md` | Decisiones con fecha: qué pasó, qué quedó, cuándo; y qué instrucción sigue cuando dos chocan. |
| `feedback.md` | Registro de los criterios que el dueño guarda mientras usa la carpeta, con fecha y caso. |

### Por dónde se empieza

La carpeta empieza usable con `guia.md`, `identidad.md`, `formas.md` y una capacidad en `tareas/`; la capacidad puede escribirse al hacer la primera pieza. Después entran `casos.md`, `identidad-visual.md`, `mirada.md`, `audiencias.md`, `territorio.md` y `arquitectura.md`, a medida que una tarea los pide. `representacion.md` entra cuando otra IA tenga que describir al dueño. Los resguardos entran cuando una pieza toca precios, datos, terceros o normas, y se mantienen cortos. En el modo persona, `rol.md` y `con-quien-trabajo.md` entran cuando el trabajo los necesita. Cada archivo suma material para nuevas piezas.

La base puede crecer por etapas. `guia.md` indica qué materiales están disponibles y qué se puede sumar después; una primera aplicación permite empezar a trabajar con lo que ya hay.

### Criterio de admisión de archivos nuevos

Un archivo nuevo tiene sentido cuando abre una capacidad, organiza materiales que necesitan un lugar propio o resuelve una necesidad observada en uso. Se acompaña con una aplicación concreta que muestre para qué sirve. Cuando alcanza con ampliar un archivo existente, se empieza ahí. Las decisiones sobre el formato se registran en [decisiones.md](decisiones.md); cada persona puede extender su carpeta según el trabajo que quiere hacer.

No todos los archivos aplican a todos los casos. Un perfil profesional puede omitir territorio, arquitectura e identidad visual; una marca omite `rol.md`. La omisión se declara en `guia.md`, nunca se disimula.

## La carpeta de trabajo

Desde la v2.0 el estándar describe también la carpeta en la que la IA trabaja todos los días. La carpeta de contexto queda adentro, visible, con el nombre `contexto/`, para que la persona la encuentre en su explorador de archivos. En un repositorio de código puede seguir oculta como `.contexto/`.

```
mi-carpeta/
├── AGENTS.md        cómo trabaja la IA en esta carpeta
├── CLAUDE.md        trae AGENTS.md y contexto/guia.md en las apps de Claude
├── LEEME.md         la explicación para la persona
├── sesion.md        la conversación que arma el contexto
├── auditoria.md     la revisión periódica
├── pasos.md         los pasos para darle más trabajo a la IA
├── contexto/        la carpeta de contexto: documentos y tareas/
└── trabajo/         lo que la IA produce
    ├── registro.md  lo hecho y lo pendiente
    └── <asunto>/    una carpeta por cliente o proyecto, con su estado.md
```

| Archivo | Qué trae |
|---|---|
| `AGENTS.md` | El método: qué lee la IA antes de trabajar, cómo trabaja, qué aprueba la persona y cómo se cierra cada trabajo. Es el archivo que leen los agentes por convención. |
| `CLAUDE.md` | Dos líneas que traen `AGENTS.md` y `contexto/guia.md` en las apps de Claude. |
| `LEEME.md` | La explicación para la persona: cómo se empieza y qué hay en la carpeta. |
| `sesion.md` | La conversación con la que la IA arma el contexto: pregunta, la persona cuenta y la IA escribe los documentos. |
| `auditoria.md` | La revisión periódica: ordena la carpeta, saca lo que quedó viejo y propone qué sumar. |
| `pasos.md` | Los pasos por los que una persona le va pasando más trabajo a su IA, con la señal que indica cuándo proponer cada uno. |
| `contexto/` | La carpeta de contexto que define este estándar. |
| `trabajo/` | Lo que la IA produce. `registro.md` lleva lo hecho y lo pendiente. Cada cliente o proyecto tiene su carpeta con un `estado.md`: quiénes participan, qué se acordó, qué está hecho y qué falta. |

### Cómo se trabaja en ella

Son seis reglas. El texto completo está en `AGENTS.md`.

1. **Primero se lee.** Antes de responder, la IA lee `contexto/guia.md`. Si el pedido corresponde a una capacidad, lee su `SKILL.md`. Si es de un cliente o proyecto con carpeta propia, lee su `estado.md`.
2. **El trabajo queda guardado.** Lo que la persona va a retomar o reutilizar queda en un archivo dentro de `trabajo/`.
3. **Cada corrección se escribe una sola vez, en su lugar.** Cómo se hace una tarea, en su skill. Cómo escribe la persona, en `formas.md`. Cómo quiere que la ayuden y qué permisos dio, en `guia.md`. Un dato nuevo, en el documento que corresponda. Una decisión que rige de ahí en adelante, en `logica.md`, con fecha.
4. **Lo que sale de la carpeta se aprueba.** Antes de mandar, publicar, pagar, borrar o cambiar algo fuera de la carpeta, la IA muestra qué va a hacer y espera el sí. Un permiso permanente se anota en `guia.md` con la fecha y las palabras de la persona.
5. **Cada trabajo se cierra.** La IA actualiza el estado del cliente o proyecto y el registro, y le cuenta a la persona qué dejó escrito.
6. **Tres palabras.** «empecemos» arma el contexto con `sesion.md`. «sumemos» agrega una capacidad o un documento. «revisemos» ordena la carpeta con `auditoria.md`.

`guia.md` declara el estado de la carpeta: «sin empezar», «sesión a medio hacer» con la lista de lo que quedó sin contar, o completa, con el paso de `pasos.md` en el que está la persona.

La carpeta lista para usar está en [`carpeta/`](carpeta/) de este repositorio. Es la misma que entrega [Trama](https://www.ideasaumentadas.com.ar/trama). Trae once skills de base en `contexto/tareas/`, para las tareas más comunes: sirven desde el primer día y se ajustan a la persona con el uso.

Una carpeta `.contexto/` sola, cargada en un proyecto de chat o en un repositorio, sigue siendo válida. La carpeta de trabajo es la forma completa, para quien usa una app que lee y escribe archivos en su computadora.

## Los principios

Lo que hace que una carpeta sea `.contexto/` son estos diez principios, antes que los nombres de archivo.

**1. El potencial va primero.** La carpeta existe para abrir capacidades: cosas que una persona o una marca puede hacer, decir, usar o mostrar con IA. Los antecedentes sirven como material de partida, no como frontera de lo posible.

**2. Materiales reales, direcciones explícitas.** La base reúne textos, referencias, casos, recursos y las posibilidades que el dueño quiere explorar. Las citas conservan sus palabras; los hechos llevan su fuente y las propuestas se presentan como propuestas. También puede orientar trabajo que todavía no se hizo.

**3. Estados honestos.** Cada campo declara su estado: cerrado, extracción parcial, baja definición, o vacío declarado. Sobre un campo no cerrado la IA no inventa hechos: pregunta, propone una hipótesis rotulada o marca el hueco.

**4. Las decisiones del dueño quedan con fecha.** Cuando el dueño corrige una pieza o fija un criterio, la carpeta lo guarda como caso: qué pasó, qué quedó, cuándo. La próxima pieza arranca sabiendo eso.

**5. Los hechos se comprueban antes de salir.** Precios, nombres, cifras, fechas y formatos de entrega tienen un lugar donde verificarse, y la carpeta dice cuál es para cada uno.

**6. Cuando dos instrucciones chocan, la carpeta dice cuál sigue.** Un criterio nuevo del dueño reemplaza al anterior; una condición de datos o de terceros se cumple antes que una preferencia de estilo.

**7. La carpeta es la base, no el libreto.** La IA crea desde estos documentos sin recitarlos ni tratarlos como un techo. Una primera pieza pone la carpeta en uso y abre el trabajo que sigue.

**8. Hacia dónde mira.** La identidad incluye su atención. `mirada.md` codifica qué observa, con qué lente lo lee y qué nuevos materiales puede traer a la creación.

**9. Primera y tercera persona separadas.** La carpeta sirve para que una IA trabaje con el dueño, y también puede ofrecer material factual para que un agente ajeno lo describa. Son dos usos distintos y no se mezclan.

**10. La carpeta se amplía con el uso.** Cada aplicación puede sumar material, ajustar una instrucción o abrir una capacidad. `feedback.md` permite guardar aprendizajes con fecha y caso; el dueño decide cuáles pasan a `formas.md`, `tareas/` o `verificacion.md`.

## Cómo se instala

Con una app que trabaja sobre las carpetas de la computadora (la app de escritorio de Claude en su pestaña Code, Codex y los agentes que leen `AGENTS.md`): se abre la app en la carpeta de trabajo. `AGENTS.md` y `CLAUDE.md` ya ordenan leer `contexto/guia.md` primero. Donde la app no cargue esos archivos por su cuenta, la primera línea de la conversación es «leé AGENTS.md y seguilo».

En plataformas de chat (ChatGPT, Claude, Gemini): un proyecto o asistente propio, la carpeta como archivos de conocimiento, y un bloque de instrucciones que ordene leer `guia.md` primero. En editores y agentes de código (Cursor, Claude Code): la carpeta en la raíz del proyecto, y una línea en el archivo de reglas del agente: "Antes de trabajar conmigo, leé `.contexto/guia.md`".

## Cómo se publica

Toda la carpeta es privada por defecto: `logica.md` y `restricciones.md` gobiernan decisiones y no son material de terceros. El único archivo escrito para afuera es `representacion.md`, y para ese el estándar recomienda cuatro movimientos, en orden de efecto comprobable.

**Reflejar las descripciones aprobadas en los datos estructurados de tu sitio.** Es la única vía con consumidores reales hoy. En schema.org, `description` para la aprobada, `disambiguatingDescription` para con qué se te confunde, `slogan`, `knowsAbout` y `subjectOf` apuntando al archivo.

**Publicar el archivo en `/.well-known/representacion.md`** de tu dominio, con el prefijo que define la [RFC 8615](https://www.rfc-editor.org/rfc/rfc8615.html).

**Enlazarlo desde el HTML** con `<link rel="alternate" type="text/markdown" href="/.well-known/representacion.md">`, que es el mecanismo con el que la web declara representaciones alternativas de un recurso desde hace décadas.

**Sumarlo al sitemap**, para que los rastreadores que ya recorren tu sitio lo encuentren.

Los tres últimos son una apuesta, y conviene decirlo con todas las letras: al agosto de 2026 ningún proveedor grande de modelos declara leer archivos de contexto publicados en un dominio. La medición pública de `llms.txt`, que tiene bastante más adopción que cualquier formato de identidad, registró 408 accesos sobre 500 millones de visitas de bots de IA en noventa días. Publicar no consigue que te lean; consigue que haya qué leer cuando alguien mira, y hoy quien mira suele ser una persona que le pasa tu dirección a su asistente.

## Cómo crear la tuya

Las plantillas de la carpeta `plantillas/` de este repositorio tienen la estructura de cada archivo con guía adentro, para armarla a mano. En `ejemplo/` está la carpeta completa de Sole, y en `carpeta/`, la carpeta de trabajo lista para usar. Para usarla desde el primer día están `system-prompt.txt`, `instalacion.md` y `auditoria.md`, que revisa la carpeta contra los diez principios y propone la próxima capacidad útil.

La manera asistida es [Trama](https://www.ideasaumentadas.com.ar/trama), de Ideas Aumentadas: la carpeta de trabajo de este estándar, gratis, que se descarga con los primeros documentos ya escritos a partir de cuatro preguntas.

## Cómo se relaciona con los otros formatos

La categoría tiene varios formatos vivos. [interoperabilidad.md](interoperabilidad.md) es el mapa completo: el terreno en tres capas, las tablas de equivalencia contra el personal context portfolio de Whittemore, Creed, me.md, el Brand Context Protocol, brand.md y brandbook.md, qué cubre cada formato que los otros no, y notas de migración en ambas direcciones. Incluye lo que a este estándar le falta hoy y lo que excluye a propósito, porque el principio de estados honestos también aplica al estándar mismo. English version: [interoperabilidad.en.md](interoperabilidad.en.md). Y para usar la carpeta dentro de un sistema personal completo: [guias/lifeos.md](guias/lifeos.md), el mapeo archivo por archivo hacia LifeOS ([English](guias/lifeos.en.md)).

## Versionado

Los cambios del estándar se registran en este archivo, con su fecha.

- **v2.0 (2026-11-10).** Versión mayor, porque cambia qué describe el estándar: de la carpeta de contexto a la carpeta de trabajo entera. El estándar suma la carpeta de trabajo: la carpeta en la que la IA trabaja todos los días, con `contexto/` adentro, `trabajo/` para lo producido y los archivos que ordenan el método (`AGENTS.md`, `CLAUDE.md`, `sesion.md`, `auditoria.md`, `pasos.md`). Quedan escritas seis reglas: qué se lee antes de trabajar, dónde se guarda el trabajo, dónde queda cada corrección, qué se aprueba antes de salir de la carpeta, cómo se cierra un trabajo y las tres palabras que abren cada momento. La carpeta lista para usar se publica en `carpeta/` y es la que entrega Trama. Las carpetas `.contexto/` existentes siguen siendo válidas sin cambios. Por qué: las apps de IA pasaron a trabajar sobre las carpetas de la computadora, y un contexto bien escrito rinde más cuando viene con el lugar donde queda el trabajo y con la manera de trabajar.
- **v1.6 (2026-10-12).** La carpeta se ordena por lo que una IA usa para crear: nueve archivos de material y la carpeta de capacidades, en el orden en que una tarea los pide. `restricciones.md`, `verificacion.md` y `logica.md` acompañan como resguardos opcionales, cortos y al final, y los principios 4, 5 y 6 se escriben desde su uso: decisiones con fecha, hechos que se comprueban y qué instrucción sigue cuando dos chocan. Es la forma que Trama entrega desde el 11-oct y la que tienen las carpetas de Ideas Aumentadas, Fonchi y Orkos. Por qué: una carpeta que una IA usa para crear rinde más cuando lo primero que encuentra es el material y lo que puede hacer con él; los resguardos siguen cuidando hechos y datos, en el lugar que les corresponde.
- **v1.5 (2026-10-11).** La carpeta pasa a organizarse desde su potencial operativo: contexto y materiales que abren capacidades para hacer, decir, usar y mostrar con IA. `tareas/` conserva nombre y formato por compatibilidad, pero cada entrada se entiende como una capacidad ampliable. La primera aplicación deja de ser una prueba final de fidelidad y pasa a demostrar que la base ya se puede usar. `identidad-visual.md` detalla composición, alineación, tipografía, logo, recursos y referencias. Los resguardos factuales, la privacidad y las normas permanecen; dejan de funcionar como centro narrativo del producto.
- **v1.4 (2026-10-01).** El estándar suma `tareas/`: una carpeta por tarea, cada una con su `SKILL.md`, en el formato de skills. El modo persona suma `con-quien-trabajo.md`. Dos archivos toman nombres más directos: `casos.md` (era `evidencia.md`) e `identidad-visual.md` (era `visual.md`); las carpetas existentes siguen siendo válidas con los nombres anteriores. El ejemplo de Sole trae una tarea.
- **v1.3 (2026-10-01).** El estándar suma «Para empezar»: los tres archivos con los que una persona arranca, cómo cargarlos y cómo se mantienen. El noveno principio describe cómo la carpeta se actualiza con el uso, y `feedback.md` pasa a ser un registro opcional de criterios del dueño. `system-prompt.txt`, la plantilla de `feedback.md` y el ejemplo de Sole acompañan.
- **v1.2 (2026-08-29).** El estándar suma cómo se mantiene afinada una carpeta mientras se usa. Cuatro prácticas entran como reglas de archivos existentes, ninguna como archivo nuevo. En `formas.md`: las muestras se marcan como luz y no como molde, y la sección de patrones de IA pasa a llamarse el registro del modelo, que nace casi vacío y se llena operando. En `mirada.md`: lo que entra de afuera pasa por `formas.md` antes de volverse texto. En `feedback.md` y el noveno principio: el ciclo de promoción, de corrección a prohibición y de ahí a caso corrible; el ejemplo de Sole lo muestra. En `guia.md`: dos reglas de operación, las instrucciones del dueño dirigen sin recitarse en lo producido, y una tanda se relee entera antes de salir. Por qué: una carpeta que se usa todos los días necesita saber cómo seguir afinada. El detalle de cada evaluación está en [decisiones.md](decisiones.md).
- **Pasada de verificación de la mirada (2026-08-17).** El estándar no cambia; la suite aprende a probar su séptimo principio. La plantilla de verificación pide un caso de pedido abierto, sin tema, cuya respuesta esperada pasa por `mirada.md` y por un hallazgo con fecha, y el ejemplo de Sole lo demuestra. Por qué: la mirada nació de una falla observada en uso, contenido que solo hablaba del sujeto, y una capa que nació de una falla necesita en la suite el caso que la detecte si vuelve.
- **v1.1 (2026-08-15).** El estándar tiene puerta en inglés: `README.en.md` y la segunda edición del mapa traducida. La categoría se escribe en inglés y ninguno de los formatos comparados es nativo en español, así que el español queda como diferencial y la puerta deja de faltar. Se cierran además las dos decisiones que quedaban del mapa de julio. Integridad: `instalacion.md` documenta cómo generar y verificar `SHA256SUMS`, y este repositorio publica el suyo; la firma criptográfica queda declarada fuera de alcance. Publicación: el estándar recomienda dónde y cómo publicar `representacion.md`, con el efecto real de cada vía declarado en vez de prometido.
- **v1.1 (2026-08-14).** Entra `mirada.md` como archivo núcleo y la atención como séptimo principio: una identidad codificada sin mirada solo puede hablar de sí. Entra `rol.md` para el modo persona, con la categoría "qué NO estoy priorizando" y su tradeoff, que hasta ahora era el hueco más señalado del formato. Y cada archivo suma frontmatter de procedencia y frescura (`status`, `generated`, `stale_after`, y `sources` cuando el archivo se deriva de otra fuente), compatible con el Open Knowledge Format. Entra `representacion.md` y con él la separación entre primera y tercera persona como noveno principio: las respuestas sobre un sujeto ya se están dando en asistentes que no son suyos, y sin este archivo se arman con lo que haya. `formas.md` clasifica sus prohibiciones por clase (palabra, estructura, apertura, cierre), porque las estructurales se cuelan cuando todas se leen al mismo nivel. `identidad.md` suma qué cuesta sostener cada convicción, y `visual.md` suma dónde viven los tokens y la regla de que viajen dentro de la carpeta cuando se entrega. Por qué: un derivado que quedó atrás de su fuente se opera igual que uno vigente, sin manera de notarlo, y el caso que originó la regla pasó en la carpeta de referencia de este estándar.

- **v1.0 (2026-07-20).** Primera versión pública: once archivos núcleo más `feedback.md`, siete principios, plantillas y ejemplo.
- **Materiales ampliados (2026-07-22).** El estándar no cambia; se completan sus materiales: el ejemplo de Sole pasa de tres archivos a la carpeta entera (con las omisiones declaradas en su `guia.md`, demostrando esa regla), y se suman `system-prompt.txt`, `instalacion.md` y `auditoria.md`. Por qué: un formato se aprende por su ejemplo, y el ejemplo estaba por un tercio.
- **Mapa de interoperabilidad (2026-07-27).** El estándar no cambia; se publica `interoperabilidad.md` (con versión en inglés): equivalencias con los otros tres formatos vivos de la categoría, ausencias propias divididas en pendiente para v1.1 y excluido por diseño, y notas de migración en ambas direcciones. Por qué: un estándar abierto se vuelve confiable cuando muestra el mapa completo, incluido dónde pierde.

## Licencia y atribución

Este estándar se publica bajo [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es): usalo, adaptalo y redistribuilo, con atribución a Ideas Aumentadas. Ver `LICENSE.md`.

Si el estándar te sirve, una estrella en [el repositorio](https://github.com/f0nchi/contexto-estandar) ayuda a que más gente lo encuentre.
