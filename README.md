# El estándar .contexto/

**Versión 2.1 · 17 de noviembre de 2026 · Mantenido por [Ideas Aumentadas](https://www.ideasaumentadas.com.ar) · CC BY 4.0**

Una estructura abierta, en español, para organizar el contexto, los materiales y las capacidades de una persona, marca o equipo en archivos de texto que puedan leer y ampliar distintas herramientas de IA.

Repositorio: [contexto-estandar](https://github.com/f0nchi/contexto-estandar) · [Página del estándar](https://www.ideasaumentadas.com.ar/estandar) · [English](README.en.md)

## Para qué sirve

La carpeta reúne una base propia: quién trabaja, qué quiere hacer, con qué materiales cuenta y qué criterios orientan su trabajo. La guía permite encontrar lo pertinente para cada caso. Los archivos son legibles y editables por su dueño y pueden llevarse a otra herramienta.

El estándar define esa estructura y el significado de sus partes. Cada persona elige cómo construirla y trabajar con ella. [Trama](https://www.ideasaumentadas.com.ar/trama) es una implementación abierta de Ideas Aumentadas: entrega la carpeta con el método, la conversación inicial y las skills de base. Esos recorridos pertenecen a Trama y se distribuyen por separado.

## Para usarlo

Creá una carpeta `contexto/` y usá [guia.md](plantillas/guia.md) como entrada. Ahí indicás a quién corresponde y qué archivos hay, con una línea sobre cada uno. Podés empezar con la información y los materiales que ya tenés.

Las [plantillas](plantillas/) están disponibles para organizar lo que vayas incorporando. Elegí las que sirven a tu trabajo. Por ejemplo, una muestra de escritura puede ir en `formas.md`; las instrucciones para una tarea, en `tareas/`. La guía permite encontrarlas. El [ejemplo completo](ejemplo/LEEME.md) muestra cómo se relacionan.

Para trabajar con una IA, dale acceso a esa carpeta e indicá que su entrada es `guia.md`. [Cómo dar acceso y conservar los cambios](instalacion.md).

## La estructura

La carpeta puede llamarse `contexto/` o `.contexto/`. Su entrada es `guia.md`: identifica a quién corresponde, qué contiene, qué está incompleto y dónde encontrar cada material o capacidad.

```text
contexto/
├── guia.md
├── identidad.md
├── formas.md
└── tareas/
    └── nombre-de-la-capacidad/
        └── SKILL.md
```

Es una base posible para empezar, no una lista que haya que completar antes de trabajar. `guia.md` permite interpretar el estado real de la carpeta. Los demás documentos se incorporan cuando sirven al caso; las omisiones pertinentes se declaran allí. Los nombres definidos se conservan para reconocer su contenido entre carpetas.

| Archivo | Qué organiza |
|---|---|
| `guia.md` | Dueño y alcance de la base, índice de materiales y capacidades, estado y referencias necesarias para usarla. |
| `identidad.md` | Qué hace, para quién, en qué está y qué quiere poder hacer. |
| `formas.md` | Cómo escribe y habla, con muestras reales y criterios propios. |
| `tareas/<nombre>/SKILL.md` | Una capacidad: para quién, qué permite hacer, materiales, instrucciones y referencias. |
| `casos.md` | Hechos, datos y casos disponibles, con su procedencia. |
| `identidad-visual.md` | Colores, tipografías, composición y ubicación de recursos visuales. |
| `mirada.md` | Referencias, fuentes y preguntas desde las que observa y explora. |
| `audiencias.md` | Personas o grupos y las situaciones en las que se relacionan con la marca o el trabajo. |
| `territorio.md` | Temas, escenas y preguntas que puede desarrollar. |
| `arquitectura.md` | Rutas de creación que relacionan materiales y posibles aplicaciones. |
| `rol.md` | Responsabilidades, semana real, decisiones y límites de un rol. |
| `con-quien-trabajo.md` | Personas o roles con quienes trabaja y contexto de esas relaciones. |
| `representacion.md` | Información aprobada para que alguien describa al dueño desde afuera. |
| `logica.md` | Decisiones con fecha, alcance y razones; precedencia cuando hay tensiones. |
| `restricciones.md` | Condiciones de datos, privacidad, terceros y otras obligaciones pertinentes. |
| `verificacion.md` | Qué hechos o condiciones deben comprobarse y dónde se verifica cada uno. |
| `feedback.md` | Observaciones por interpretar o confirmar, cuando hace falta conservarlas antes de incorporarlas. |

La carpeta puede convivir con proyectos, resultados e historiales. La guía indica dónde están los materiales pertinentes. El estándar no exige nombres para esas carpetas externas, una entrevista, palabras de inicio, una frecuencia de revisión ni una secuencia de delegación.

## Capacidades

Cada capacidad tiene su carpeta dentro de `tareas/` y un `SKILL.md`. El encabezado identifica su nombre y cuándo se usa:

```yaml
---
name: nombre-de-la-capacidad
description: "Cuándo sirve esta capacidad."
---
```

El cuerpo permite entender para quién es, qué puede producir o mover y con qué materiales e instrucciones trabaja. Puede incluir procedimiento, criterios de calidad con su alcance, formato y referencias a aplicaciones previas. Una capacidad nueva puede empezar como propuesta; una referencia aprobada se identifica como tal. Los ajustes se integran donde cambia la instrucción y pueden llevar un registro breve con fecha.

La [plantilla](plantillas/tareas/nombre-de-la-tarea/SKILL.md) ofrece una forma de escribirla. El catálogo de capacidades y su procedimiento pertenecen a cada implementación. No hay una cantidad obligatoria de skills ni un campo obligatorio de «primera aplicación» ya completado.

## Principios

1. **El potencial va primero.** El contexto permite abrir capacidades. La experiencia y los materiales son puntos de partida para lo que se quiere hacer.
2. **Materiales reales, direcciones explícitas.** Los hechos conservan su procedencia; las propuestas se identifican. La carpeta también admite posibilidades todavía sin desarrollar.
3. **Estados honestos.** Lo incompleto, lo provisional y lo confirmado se distinguen. Los huecos se declaran sin inventar información.
4. **Criterios con fecha y alcance.** Una decisión conserva a qué trabajo, persona o situación aplica. Su razón y el caso de origen se incluyen cuando ayudan a interpretarla.
5. **Hechos comprobables.** Los datos relevantes tienen una fuente o un lugar donde verificar su vigencia.
6. **Precedencia explícita.** Una instrucción nueva reemplaza la anterior dentro de su alcance. Las contradicciones pendientes quedan identificadas.
7. **La carpeta es una base para crear.** Sus materiales y ejemplos permiten desarrollar aplicaciones nuevas; se interpretan según el caso.
8. **Una mirada propia.** Las referencias y preguntas de su dueño pueden orientar lo que observa y explora.
9. **Usos diferenciados.** Trabajar con el dueño y describirlo ante terceros requieren materiales y permisos adecuados a cada uso.
10. **La base puede crecer.** Las aplicaciones pueden ampliar materiales, criterios y capacidades. Las decisiones adoptadas se integran en su lugar; las observaciones por confirmar conservan ese estado.

Estos principios orientan la estructura. Su aplicación puede darse conversando, escribiendo a mano o mediante herramientas distintas.

## Estado, procedencia y alcance

La información puede expresarse en Markdown corriente: una fecha, una fuente, una aclaración de estado o de alcance. El bloque YAML de las plantillas es una opción para quien necesite metadatos estructurados; `status`, `stale_after` y los demás campos no son requisitos universales. El encabezado de las skills conserva su función propia de identificación.

Una instrucción adoptada tiene un lugar vigente. `feedback.md` es opcional: sirve para conservar observaciones pendientes de interpretación, sin obligar a duplicar todas las decisiones. Una idea por explorar se distingue de un compromiso de trabajo.

Si una base reúne varios clientes o proyectos, cada contexto declara a quién corresponde y la guía indica cuándo consultarlo. Una preferencia de un cliente conserva ese alcance. El estándar permite contextos separados y referencias entre ellos; la organización concreta depende del trabajo.

## Extender y conservar

Un archivo nuevo tiene sentido cuando organiza un material o capacidad que los existentes no pueden recibir claramente. La guía explica su propósito y ubicación. Se puede ampliar un documento existente antes de crear otro.

Las carpetas anteriores siguen siendo válidas, incluidos los nombres históricos `evidencia.md` y `visual.md` si la guía los identifica. Las carpetas de trabajo de v2.0 pueden seguir funcionando con su método; en v2.1 ese método se reconoce como implementación y deja de ser un requisito del formato.

Una copia o un historial recuperable ayuda a conservar el trabajo al reorganizarlo. Cada implementación elige cómo hacerlo. Las conexiones, automatizaciones y permisos de las herramientas están fuera del formato.

## Materiales para usarlo

- [Plantillas](plantillas/): estructuras con indicaciones que se reemplazan por contenido propio.
- [Ejemplo de Sole](ejemplo/LEEME.md): una analista ficticia con materiales y una capacidad desarrollada. Sus decisiones ilustran un uso; no son requisitos para otras carpetas.
- [Instalación](instalacion.md): cómo dar acceso a los archivos y distinguir lectura de actualización.
- [Instrucción de ejemplo](system-prompt.txt): una entrada breve y opcional para una IA.
- [Revisión de estructura](auditoria.md): comprobar que la base sea comprensible y consistente.
- [Decisiones](decisiones.md): historia de las elecciones del formato.

[Interoperabilidad](interoperabilidad.md) y [LifeOS](guias/lifeos.md) conservan comparaciones y guías con su fecha; son material complementario, no requisitos del estándar.

## Abierto y propio

El documento, las plantillas y el ejemplo se publican bajo [CC BY 4.0](LICENSE.md): se pueden usar, adaptar y compartir con atribución a Ideas Aumentadas. El contenido que una persona agrega conserva su titularidad y privacidad. La estructura no publica archivos ni concede acceso a terceros.

Trama comparte su método completo con su propia descarga y licencia. Se puede usar este estándar sin Trama, y se puede adaptar Trama según el trabajo de cada persona.

## Historial de versiones

Los cambios se registran con su fecha. Las entradas anteriores describen lo que definía cada versión en su momento.

- **v2.1 (2026-11-17).** El estándar queda definido como estructura, principios y significado de sus documentos. El método conversacional y la carpeta operativa se distribuyen en Trama. Se aclaran los estados, el alcance de los criterios, el carácter opcional de los metadatos y las extensiones. Las carpetas existentes mantienen su validez.
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
