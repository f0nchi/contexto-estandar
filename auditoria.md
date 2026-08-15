# Auditoría de cumplimiento

> Parte del estándar .contexto/ · v1.1
> El estándar se define por nueve principios, y una carpeta puede auditarse contra ellos. Cualquier IA que haya leído tu carpeta puede correr esta auditoría: es la verificación corrible, aplicada al estándar mismo.

Pegale esto a una IA que ya tenga tu carpeta cargada:

---

Auditá mi carpeta .contexto/ contra los nueve principios del estándar (github.com/f0nchi/contexto-estandar). Para cada principio, respondé: cumple, parcial o falta, con el ejemplo concreto de mi carpeta que lo demuestra.

1. Casos reales, frases literales: ¿cada entrada tiene un caso que pasó y citas textuales mías? Marcá las entradas que son autodefinición sin caso: esas todavía no son contenido.
2. Estados honestos: ¿cada campo declara su estado? ¿Hay campos vacíos sin declarar, u omisiones disimuladas que guia.md no nombra?
3. Jurisprudencia con fecha: ¿las decisiones tienen su caso, su regla y su cuándo?
4. Verificación corrible: ¿verificacion.md existe y sus casos se pueden correr de verdad? Corré dos y mostrame el resultado.
5. Precedencia explícita: ¿la carpeta dice qué manda cuando dos reglas chocan? Buscá dos reglas mías que podrían chocar y decime si la carpeta resuelve el choque.
6. La carpeta es la lente, no el libreto: ¿hay contenido que describe el método o los límites en vez de operar desde ellos?
7. Hacia dónde mira: ¿mirada.md existe? ¿Sus universos de atención se pueden rastrear hasta una convicción o una decisión escrita en otro archivo, o son una lista de temas de actualidad? ¿La lente está escrita como preguntas aplicables a un hecho nuevo, y podría firmarlas otro del mismo rubro sin cambiar nada? ¿Hay señales declaradas que irían en contra de la propia tesis?
8. Primera y tercera persona: ¿existe representacion.md? ¿Sus descripciones aprobadas están en los tres largos, listas para copiar? ¿Hay material de tercera persona mezclado en los archivos de primera, o al revés?
9. Memoria de correcciones: ¿feedback.md existe y tiene entradas con fecha, regla y ejemplo?

Además, para cada archivo: ¿el frontmatter declara `status` y `stale_after`? Si el archivo se deriva de otra fuente, ¿declara `sources` con su fecha? Marcá los derivados cuya fuente se movió después de la derivación: se operan igual que los vigentes y nadie lo nota.

Cerrá con los tres arreglos de mayor impacto, en orden, y para cada uno decime qué archivo tocar.

---

El resultado no es un puntaje: es un mapa de dónde tu carpeta todavía es declaración y dónde ya es sistema. Los arreglos casi siempre son el mismo movimiento: menos definición, más caso.
