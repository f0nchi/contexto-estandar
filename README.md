# El estándar .contexto/

**Versión 1.1 · 14 de agosto de 2026 · Mantenido por [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · Licencia CC BY 4.0**

Una convención abierta, en español, para codificar la inteligencia de trabajo de una persona o una marca en una carpeta de archivos de texto plano que cualquier IA puede leer y operar.

Repositorio canónico: https://github.com/f0nchi/contexto-estandar · Página del estándar: https://www.ideasaumentadas.com.ar/estandar

## Por qué una carpeta de texto plano

La inteligencia de un trabajo existe: está en cómo decidís, en qué podés afirmar, en lo que nunca harías, en la lógica detrás de cada posición tomada. Cuando esa inteligencia queda escrita en markdown plano, pasa tres pruebas a la vez: cualquier IA la lee nativamente, cualquier humano la puede abrir y editar, y es tuya para siempre, portable entre plataformas, sin lock-in de ningún proveedor.

Este estándar define cómo organizarla para que una IA no solo la lea: la opere.

## La carpeta

Una carpeta `.contexto/` tiene trece archivos núcleo, uno de crecimiento y uno propio del modo persona:

| Archivo | Qué codifica |
|---|---|
| `guia.md` | Punto de entrada: qué es la carpeta, orden de lectura, reglas de operación, estado de la versión. |
| `identidad.md` | Por qué existe este trabajo o esta marca, qué mundo empuja, qué no debe perder. Para personas: también el momento vigente. |
| `mirada.md` | Hacia dónde mira: universos de atención, la lente con la que lee un hecho nuevo, de qué se alimenta, y qué evidencia iría en contra de su propia tesis. |
| `formas.md` | Cómo escribe y habla: síntesis, muestras reales de así sí y así no, prohibiciones con su reemplazo, tono por contexto. |
| `territorio.md` | De qué habla, de qué no, dónde está la frontera, niveles de conversación. |
| `audiencias.md` | Perfiles reales con caso vivido, para quién no es. Para personas: relaciones de trabajo. |
| `arquitectura.md` | Pilares que sostienen el contenido, estructuras que ya funcionaron. |
| `restricciones.md` | Qué nunca haría, condiciones operativas, estados de promesa. |
| `logica.md` | Jurisprudencia: casos reales con fecha y porqué, reglas, y qué manda cuando dos reglas chocan. |
| `evidencia.md` | Casos comprobables, qué es afirmable y qué todavía no, qué promesas están permitidas. |
| `visual.md` | El sistema visual si existe. Si no existe, se declara: ninguna IA debe inventar uno. |
| `representacion.md` | Qué puede decir de este sujeto una IA que no trabaja para él: descripciones aprobadas, con qué se confunde, qué nunca decir, y las trampas de encuadre. |
| `verificacion.md` | La suite de pruebas de la identidad: casos corribles por cualquier IA. |
| `rol.md` | Solo personas: cómo son las semanas de verdad, con quién, qué decide, qué delega, y qué NO está priorizando con su tradeoff. |
| `feedback.md` | El archivo que crece con el uso: cada corrección del dueño, en una línea con fecha, regla y ejemplo. |

### Por dónde se empieza

La carpeta se construye en orden, y el orden importa porque los primeros archivos sostienen a los que siguen: `guia.md`, `identidad.md`, `formas.md`, `restricciones.md`, `logica.md` y `verificacion.md` son los que dan la primera vuelta completa, con el sujeto, su forma de escribir, sus límites, su forma de decidir y la manera de comprobar que una IA lo está operando bien. Después entran `mirada.md`, `territorio.md`, `audiencias.md`, `arquitectura.md`, `evidencia.md`, `visual.md`, `representacion.md` y, en el modo persona, `rol.md`. `feedback.md` empieza a llenarse desde el primer día de uso.

Una carpeta a mitad de camino es un estado legítimo y se declara en `guia.md`. Lo que no es legítimo es dejar afuera algo que el sujeto sí tiene: la omisión vale cuando el campo no aplica, nunca para llegar antes.

### Criterio de admisión de archivos nuevos

Este estándar crece con cuidado, y la vara para sumar un archivo es esta: responde una pregunta que ninguno de los existentes responde, nació de una falla observada en uso con su fecha y su caso, el ejemplo lo puede demostrar con contenido real, y su ausencia se nota en lo que la IA produce y no solamente en la prolijidad del esquema. Un candidato que no pasa los cuatro entra como sección de un archivo existente, y la mayoría de los candidatos son eso. Cada evaluación queda registrada en [decisiones.md](decisiones.md), incluidas las negativas: un estándar que solo muestra lo que aceptó no deja ver su vara.

No todos los archivos aplican a todos los casos. Un perfil profesional puede omitir territorio, arquitectura y visual; una marca omite `rol.md`. La omisión se declara en `guia.md`, nunca se disimula.

## Los principios

Lo que hace que una carpeta sea `.contexto/` son estas nueve reglas, antes que los nombres de archivo.

**1. Casos reales, frases literales.** Cada entrada sale de algo que pasó, con las palabras del dueño citadas textuales. Una autodefinición que serviría para cualquiera del rubro todavía no es contenido.

**2. Estados honestos.** Cada campo declara su estado: cerrado, extracción parcial, baja definición, o vacío declarado. Sobre un campo no cerrado la IA no inventa: pregunta o marca el hueco. El vacío declarado es contenido legítimo ("esta marca no tiene casos públicos todavía; la IA afirma método, no resultados").

**3. Jurisprudencia con fecha.** Las decisiones se registran como casos: qué pasó, qué regla dejó, cuándo. La regla sin su caso de origen vale menos: el caso es lo que le permite a una IA razonar situaciones nuevas.

**4. Verificación corrible.** La carpeta incluye su propia suite de pruebas: situación, respuesta esperada, qué nunca, y la regla que lo justifica. Cualquier IA que leyó la carpeta puede correrla, y el dueño puede comprobar que está siendo operado con su lógica y no improvisado.

**5. Precedencia explícita.** Cuando dos reglas chocan, la carpeta dice cuál manda y bajo qué condición. Sin precedencia, la IA promedia; y promediar es la manera más silenciosa de traicionar una identidad.

**6. La carpeta es la lente, no el libreto.** La IA escribe y decide desde estos documentos, sin describirlos ni convertir los límites, el método o los anti-ejemplos en contenido público.

**7. Hacia dónde mira.** La identidad incluye su atención. Cuando todos los archivos describen al sujeto, la única materia disponible para producir es el sujeto mismo, y una identidad codificada sin mirada solo puede hablar de sí. `mirada.md` codifica qué observa, con qué lente lo lee y qué haría cambiar de opinión al dueño.

**8. Primera y tercera persona separadas.** La carpeta sirve para que una IA escriba y decida como el dueño, y sirve para que un agente ajeno hable de él. Son dos materiales distintos y no se mezclan: lo que gobierna la escritura propia vive en toda la carpeta, y lo que un tercero puede decir vive solo en `representacion.md`, con lo que el dueño autoriza.

**9. Memoria de correcciones.** Cada corrección del dueño se propone como una línea nueva de `feedback.md`: fecha, regla aprendida, ejemplo. La identidad acumula jurisprudencia con el uso.

## Cómo se instala

En plataformas de chat (ChatGPT, Claude, Gemini): un proyecto o asistente propio, la carpeta como archivos de conocimiento, y un bloque de instrucciones que ordene leer `guia.md` primero. En editores y agentes de código (Cursor, Claude Code): la carpeta en la raíz del proyecto, y una línea en el archivo de reglas del agente: "Antes de trabajar conmigo, leé `.contexto/guia.md`".

## Cómo se publica

Toda la carpeta es privada por defecto: `logica.md` y `restricciones.md` gobiernan decisiones y no son material de terceros. El único archivo escrito para afuera es `representacion.md`, y para ese el estándar recomienda cuatro movimientos, en orden de efecto comprobable.

**Reflejar las descripciones aprobadas en los datos estructurados de tu sitio.** Es la única vía con consumidores reales hoy. En schema.org, `description` para la aprobada, `disambiguatingDescription` para con qué se te confunde, `slogan`, `knowsAbout` y `subjectOf` apuntando al archivo.

**Publicar el archivo en `/.well-known/representacion.md`** de tu dominio, con el prefijo que define la [RFC 8615](https://www.rfc-editor.org/rfc/rfc8615.html).

**Enlazarlo desde el HTML** con `<link rel="alternate" type="text/markdown" href="/.well-known/representacion.md">`, que es el mecanismo con el que la web declara representaciones alternativas de un recurso desde hace décadas.

**Sumarlo al sitemap**, para que los rastreadores que ya recorren tu sitio lo encuentren.

Los tres últimos son una apuesta, y conviene decirlo con todas las letras: al agosto de 2026 ningún proveedor grande de modelos declara leer archivos de contexto publicados en un dominio. La medición pública de `llms.txt`, que tiene bastante más adopción que cualquier formato de identidad, registró 408 accesos sobre 500 millones de visitas de bots de IA en noventa días. Publicar no consigue que te lean; consigue que haya qué leer cuando alguien mira, y hoy quien mira suele ser una persona que le pasa tu dirección a su asistente.

## Cómo crear la tuya

Las plantillas de la carpeta `plantillas/` de este repositorio tienen la estructura de cada archivo con guía adentro, para armarla a mano. En `ejemplo/` está la carpeta completa de Sole, un perfil profesional de muestra que además demuestra la regla de omisión declarada. Y para usarla desde el primer día: `system-prompt.txt` (el bloque listo para pegar en cualquier IA), `instalacion.md` (cómo cargarla en ChatGPT, Claude, Gemini y agentes de código) y `auditoria.md` (un prompt para que cualquier IA revise tu carpeta contra los nueve principios y te diga qué le falta).

La manera asistida existe en [Ideas Aumentadas](https://www.ideasaumentadas.com.ar): un primer archivo de contexto gratis en el navegador, y sesiones de extracción con un agente que trabaja con casos reales y entrega la carpeta completa con su suite de verificación.

## Cómo se relaciona con los otros formatos

La categoría tiene varios formatos vivos. [interoperabilidad.md](interoperabilidad.md) es el mapa completo: equivalencias sección por sección con el personal context portfolio de Nathaniel Whittemore, Creed y me.md, qué cubre cada formato que los otros no, y notas de migración en ambas direcciones. Incluye lo que a este estándar le falta hoy y lo que excluye a propósito, porque el principio de estados honestos también aplica al estándar mismo. English version: [interoperabilidad.en.md](interoperabilidad.en.md).

## Versionado

Los cambios del estándar se registran en este archivo, con fecha y porqué.

- **v1.1 (2026-08-15).** Se cierran las dos decisiones que quedaban del mapa de julio. Integridad: `instalacion.md` documenta cómo generar y verificar `SHA256SUMS`, y este repositorio publica el suyo; la firma criptográfica queda declarada fuera de alcance. Publicación: el estándar recomienda dónde y cómo publicar `representacion.md`, con el efecto real de cada vía declarado en vez de prometido.
- **v1.1 (2026-08-14).** Entra `mirada.md` como archivo núcleo y la atención como séptimo principio: una identidad codificada sin mirada solo puede hablar de sí. Entra `rol.md` para el modo persona, con la categoría "qué NO estoy priorizando" y su tradeoff, que hasta ahora era el hueco más señalado del formato. Y cada archivo suma frontmatter de procedencia y frescura (`status`, `generated`, `stale_after`, y `sources` cuando el archivo se deriva de otra fuente), compatible con el Open Knowledge Format. Entra `representacion.md` y con él la separación entre primera y tercera persona como noveno principio: las respuestas sobre un sujeto ya se están dando en asistentes que no son suyos, y sin este archivo se arman con lo que haya. `formas.md` clasifica sus prohibiciones por clase (palabra, estructura, apertura, cierre), porque las estructurales se cuelan cuando todas se leen al mismo nivel. `identidad.md` suma qué cuesta sostener cada convicción, y `visual.md` suma dónde viven los tokens y la regla de que viajen dentro de la carpeta cuando se entrega. Por qué: un derivado que quedó atrás de su fuente se opera igual que uno vigente, sin manera de notarlo, y el caso que originó la regla pasó en la carpeta de referencia de este estándar.

- **v1.0 (2026-07-20).** Primera versión pública: once archivos núcleo más `feedback.md`, siete principios, plantillas y ejemplo.
- **Materiales ampliados (2026-07-22).** El estándar no cambia; se completan sus materiales: el ejemplo de Sole pasa de tres archivos a la carpeta entera (con las omisiones declaradas en su `guia.md`, demostrando esa regla), y se suman `system-prompt.txt`, `instalacion.md` y `auditoria.md`. Por qué: un formato se aprende por su ejemplo, y el ejemplo estaba por un tercio.
- **Mapa de interoperabilidad (2026-07-27).** El estándar no cambia; se publica `interoperabilidad.md` (con versión en inglés): equivalencias con los otros tres formatos vivos de la categoría, ausencias propias divididas en pendiente para v1.1 y excluido por diseño, y notas de migración en ambas direcciones. Por qué: un estándar abierto se vuelve confiable cuando muestra el mapa completo, incluido dónde pierde.

## Licencia y atribución

Este estándar se publica bajo [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es): usalo, adaptalo y redistribuilo, con atribución a Ideas Aumentadas. Ver `LICENSE.md`.

Si el estándar te sirve, una estrella en [el repositorio](https://github.com/f0nchi/contexto-estandar) ayuda a que más gente lo encuentre.
