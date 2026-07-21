# El estándar .contexto/

**Versión 1.0 · 20 de julio de 2026 · Mantenido por [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · Licencia CC BY 4.0**

Una convención abierta, en español, para codificar la inteligencia de trabajo de una persona o una marca en una carpeta de archivos de texto plano que cualquier IA puede leer y operar.

Repositorio canónico: https://github.com/f0nchi/contexto-estandar · Página del estándar: https://www.ideasaumentadas.com.ar/estandar

## Por qué una carpeta de texto plano

La inteligencia de un trabajo existe: está en cómo decidís, en qué podés afirmar, en lo que nunca harías, en la lógica detrás de cada posición tomada. Cuando esa inteligencia queda escrita en markdown plano, pasa tres pruebas a la vez: cualquier IA la lee nativamente, cualquier humano la puede abrir y editar, y es tuya para siempre, portable entre plataformas, sin lock-in de ningún proveedor.

Este estándar define cómo organizarla para que una IA no solo la lea: la opere.

## La carpeta

Una carpeta `.contexto/` tiene once archivos núcleo y uno de crecimiento:

| Archivo | Qué codifica |
|---|---|
| `guia.md` | Punto de entrada: qué es la carpeta, orden de lectura, reglas de operación, estado de la versión. |
| `identidad.md` | Por qué existe este trabajo o esta marca, qué mundo empuja, qué no debe perder. Para personas: también el momento vigente. |
| `formas.md` | Cómo escribe y habla: síntesis, muestras reales de así sí y así no, prohibiciones con su reemplazo, tono por contexto. |
| `territorio.md` | De qué habla, de qué no, dónde está la frontera, niveles de conversación. |
| `audiencias.md` | Perfiles reales con caso vivido, para quién no es. Para personas: relaciones de trabajo. |
| `arquitectura.md` | Pilares que sostienen el contenido, estructuras que ya funcionaron. |
| `restricciones.md` | Qué nunca haría, condiciones operativas, estados de promesa. |
| `logica.md` | Jurisprudencia: casos reales con fecha y porqué, reglas, y qué manda cuando dos reglas chocan. |
| `evidencia.md` | Casos comprobables, qué es afirmable y qué todavía no, qué promesas están permitidas. |
| `visual.md` | El sistema visual si existe. Si no existe, se declara: ninguna IA debe inventar uno. |
| `verificacion.md` | La suite de pruebas de la identidad: casos corribles por cualquier IA. |
| `feedback.md` | El archivo que crece con el uso: cada corrección del dueño, en una línea con fecha, regla y ejemplo. |

No todos los archivos aplican a todos los casos. Un perfil profesional puede omitir territorio, arquitectura y visual: la omisión se declara en `guia.md`, nunca se disimula.

## Los principios

Lo que hace que una carpeta sea `.contexto/` no son los nombres de archivo: son estas siete reglas.

**1. Casos reales, frases literales.** Cada entrada sale de algo que pasó, con las palabras del dueño citadas textuales. Una autodefinición que serviría para cualquiera del rubro todavía no es contenido.

**2. Estados honestos.** Cada campo declara su estado: cerrado, extracción parcial, baja definición, o vacío declarado. Sobre un campo no cerrado la IA no inventa: pregunta o marca el hueco. El vacío declarado es contenido legítimo ("esta marca no tiene casos públicos todavía; la IA afirma método, no resultados").

**3. Jurisprudencia con fecha.** Las decisiones se registran como casos: qué pasó, qué regla dejó, cuándo. La regla sin su caso de origen vale menos: el caso es lo que le permite a una IA razonar situaciones nuevas.

**4. Verificación corrible.** La carpeta incluye su propia suite de pruebas: situación, respuesta esperada, qué nunca, y la regla que lo justifica. Cualquier IA que leyó la carpeta puede correrla, y el dueño puede comprobar que está siendo operado con su lógica y no improvisado.

**5. Precedencia explícita.** Cuando dos reglas chocan, la carpeta dice cuál manda y bajo qué condición. Sin precedencia, la IA promedia; y promediar es la manera más silenciosa de traicionar una identidad.

**6. La carpeta es la lente, no el libreto.** La IA escribe y decide desde estos documentos, sin describirlos ni convertir los límites, el método o los anti-ejemplos en contenido público.

**7. Memoria de correcciones.** Cada corrección del dueño se propone como una línea nueva de `feedback.md`: fecha, regla aprendida, ejemplo. La identidad acumula jurisprudencia con el uso.

## Cómo se instala

En plataformas de chat (ChatGPT, Claude, Gemini): un proyecto o asistente propio, la carpeta como archivos de conocimiento, y un bloque de instrucciones que ordene leer `guia.md` primero. En editores y agentes de código (Cursor, Claude Code): la carpeta en la raíz del proyecto, y una línea en el archivo de reglas del agente: "Antes de trabajar conmigo, leé `.contexto/guia.md`".

## Cómo crear la tuya

Las plantillas de la carpeta `plantillas/` de este repositorio tienen la estructura de cada archivo con guía adentro, para armarla a mano. En `ejemplo/` hay una carpeta mínima de muestra.

La manera asistida existe en [Ideas Aumentadas](https://www.ideasaumentadas.com.ar): un primer archivo de contexto gratis en el navegador, y sesiones de extracción con un agente que trabaja con casos reales y entrega la carpeta completa con su suite de verificación.

## Versionado

Los cambios del estándar se registran en este archivo, con fecha y porqué.

- **v1.0 (2026-07-20).** Primera versión pública: once archivos núcleo más `feedback.md`, siete principios, plantillas y ejemplo.

## Licencia y atribución

Este estándar se publica bajo [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es): usalo, adaptalo y redistribuilo, con atribución a Ideas Aumentadas. Ver `LICENSE.md`.
