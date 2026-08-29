# Decisiones del estándar

> Parte del estándar [.contexto/](README.md). El registro de qué entró, qué quedó afuera y por qué.

Cada archivo candidato se evalúa contra la vara de admisión del README: responde una pregunta que ninguno de los existentes responde, nació de una falla observada en uso con su fecha y su caso, el ejemplo lo puede demostrar con contenido real, y su ausencia se nota en lo que la IA produce. Los cuatro, o entra como sección de un archivo existente.

Acá quedan las evaluaciones, incluidas las negativas. Un estándar que solo muestra lo que aceptó no deja ver su vara.

## Aceptados

### `mirada.md` · v1.1 · 2026-08-13

**Pregunta propia:** hacia dónde mira el sujeto y con qué lente lee un hecho nuevo. Ningún archivo la responde: todos los demás describen al sujeto.
**Falla que lo originó:** 2026-08-12, el sistema de contenido de la implementación de referencia produjo piezas sobre su propio método teniendo escrita la regla que lo prohíbe. La regla prohibía sin ofrecer de dónde sacar la otra materia.
**Demostrable:** sí, en el ejemplo, con cuatro universos rastreables hasta convicciones escritas en otros archivos.
**Se nota en el output:** sí, es exactamente lo que se notó.

### `rol.md` · v1.1 · 2026-08-14

**Pregunta propia:** cómo transcurre la semana real de una persona, qué decide, qué delega y qué deja afuera a propósito. `identidad.md` responde por qué existe el trabajo y no cómo pasa.
**Falla que lo originó:** el mapa de interoperabilidad del 2026-07-27 lo declaró públicamente como hueco frente al personal context portfolio, que es más fuerte en esa dimensión.
**Demostrable:** sí, con las tres renuncias declaradas del ejemplo.
**Se nota en el output:** sí. Una IA que conoce la convicción de alguien y desconoce su semana propone cosas que no entran en ningún día real.

### `representacion.md` · v1.1 · 2026-08-14

**Pregunta propia:** qué puede decir del sujeto una IA que no trabaja para él. El resto de la carpeta sirve para hablar como el sujeto.
**Falla que lo originó:** las respuestas sobre un sujeto ya se están dando en asistentes ajenos, y sin este material se arman con lo que haya. El Brand Context Protocol lo resolvió antes y es la ausencia más señalada del formato.
**Demostrable:** sí.
**Se nota en el output:** sí, en cada descripción de terceros que erra la categoría.

## Rechazados por ahora

### Señales de mercado como archivo propio · evaluado el 2026-08-14

Registrar deseo, comprensión, confusión, uso, roce y riesgo, con su lectura y su movimiento posible.

**Pasa:** responde una pregunta que ningún archivo responde, y existe funcionando en la implementación de referencia desde el 2026-06-27.
**No pasa:** no nació de una falla observada, y su forma depende del negocio de cada sujeto, con lo cual la plantilla se convertiría en un CRM chico. Su ausencia no se nota todavía en lo que la IA produce.
**Queda:** afuera del estándar, viviendo en la operación de cada implementador. Se revisa cuando aparezca una falla concreta que lo pida.

## Resueltos como sección, no como archivo

- **Patrones de lenguaje generado por IA.** El Brand Context Protocol les da un archivo propio. Acá entraron como sección tipificada de `formas.md`, porque comparten naturaleza con el resto de las prohibiciones y separarlos hacía que se leyeran como un tema aparte.
- **Tokens de diseño en formato de máquina.** Entraron como sección de `visual.md`, con la regla de que viajen dentro de la carpeta cuando se entrega a un tercero.
- **Qué cuesta sostener cada convicción.** Idea tomada de `values.md` del Brand Context Protocol. Entró como sección de `identidad.md`.
- **Procedencia y frescura.** Entró como frontmatter de todos los archivos, sin archivo propio. Originado en una falla del 2026-08-14: un archivo derivado quedó atrás de su fuente y se operó igual que uno vigente.

## Resueltos como sección o regla · v1.2 · 2026-08-29

Los cinco nacieron de la misma semana de fallas fechadas: la carpeta de referencia operada en producción real, una tanda de catorce piezas corregida entera por el dueño en dos pasadas. Ninguno pidió archivo nuevo.

- **Los ejemplos anclan.** El modelo converge hacia las muestras y los "así sí" y los trata como molde; en el caso de origen, el ejemplo canónico de la carpeta terminó definiendo hacia abajo todas las piezas de la tanda. Entró como guía de `formas.md`: las muestras son luz, no molde.
- **El registro del modelo, con la regla de nacimiento vacío.** La sección de patrones de IA rechazados ya existía; lo que faltaba era la regla de que no se puede extraer por preguntas. Nadie puede responder "¿qué diría el modelo que vos jamás dirías?" en abstracto: el dueño del caso de origen la respondió entera en una tarde de leer piezas producidas. Entró como upgrade de esa guía de `formas.md`: nace casi vacía, se llena operando vía el ciclo de promoción.
- **Los marcos del territorio viajan pegados.** La carpeta de referencia importó el marco "llegar temprano/llegar tarde" del discurso tecnológico que su mirada monitorea, un reloj que ni el sujeto ni su audiencia usan. La ley general: cada territorio monitoreado habla con su registro, y ese registro se filtra a lo producido si `formas.md` no lo frena. Entró como guía de `mirada.md`.
- **El ciclo de promoción.** `feedback.md` acumulaba correcciones sin decir cuándo una se gradúa. La regla: feedback → prohibición con reemplazo en `formas.md` → caso corrible en `verificacion.md`, con el ascenso anotado en la línea original. El ejemplo de Sole ya lo demostraba sin nombrarlo (su corrección del 08-jul vive como prohibición y como caso 1 de la suite) y ahora lo anota. Entró en la plantilla de `feedback.md`, en la guía de `verificacion.md` y en el noveno principio.
- **La relectura de tanda.** Un motivo, una apertura o un remate repetido entre piezas no relacionadas de una misma tanda es un tic del operador, no un tema del sujeto: en el caso de origen, un mismo marco apareció en cuatro piezas y un mismo remate en tres. Entró como regla de operación de `guia.md`, junto con su hermana: las instrucciones del dueño dirigen y no se recitan en lo producido (el vocabulario de una devolución apareció textual en una pieza).

**Evaluados y no ascendidos, de la misma semana:** la escala del relato (a qué magnitud habla el sujeto de lo que construye) y la calibración entre versiones larga y corta de una pieza. Los dos son contenido de identidad de cada sujeto, no estructura: cada carpeta los resuelve en su propio `formas.md`. Y las barreras técnicas de la implementación de referencia (el lint que bloquea prohibiciones en el pipeline) quedan del lado del implementador: son la manera de esa operación de correr su suite, y el estándar sigue siendo una convención de archivos neutral.

## Excluido por diseño

- **Gobernanza multiagente y permisos por sección.** El modelo de este estándar es un dueño y su IA. Los permisos por asiento pertenecen a productos para equipos, y Creed resuelve bien esa tesis, que es otra.
- **Infraestructura propia.** Sincronización automática, scoring como servicio o conector propio. El estándar es una convención de archivos neutral; las herramientas que lo operan son otra capa, de cada implementador.

## Resueltos el 2026-08-15

### Sello de integridad

Estaba declarado "en evaluación" desde el 2026-07-27, tomado de me.md, que es el único formato de la categoría que lo ofrece.

**Resuelto como comando documentado, sin archivo ni infraestructura.** `instalacion.md` explica cómo generar `SHA256SUMS` y cómo verificarlo, en las tres plataformas, y este repositorio publica el suyo. Con eso, quien recibe una carpeta puede comprobar que llegó tal como salió.

Lo que queda declarado como fuera de alcance: la firma criptográfica, que probaría quién es el dueño y no solo que los archivos no cambiaron. Es infraestructura de quien distribuya y cada implementador la resuelve con sus herramientas.

### Descubrimiento

**Resuelto de forma parcial y declarada como tal.** El estándar recomienda publicar `representacion.md`, el único archivo escrito para terceros, en `/.well-known/representacion.md` del dominio del sujeto, enlazarlo desde el HTML con `<link rel="alternate" type="text/markdown">`, incluirlo en el sitemap, y reflejar sus descripciones aprobadas en los datos estructurados de la página.

De esas cuatro vías, la única con consumidores reales hoy son los datos estructurados. La ubicación conocida es una apuesta: al 2026-08, ningún proveedor grande de modelos declara leer archivos de este tipo, y la medición pública de `llms.txt`, que tiene mucha más adopción que cualquier formato de identidad, muestra 408 accesos sobre 500 millones de visitas de bots. El estándar lo dice con esas palabras en lugar de prometer descubrimiento.

Lo que sigue abierto: publicar la carpeta completa, que este estándar no recomienda. `logica.md` y `restricciones.md` gobiernan decisiones y no son material de terceros.

## Abierto

- **Herencia entre marca madre, producto y submarca.** `brand.md` lo resuelve con fusión de guardrails, donde un hijo endurece y nunca debilita. Falta decidir la forma acá: carpetas anidadas que heredan, o un campo de alcance dentro de cada archivo.
- **Verificación de juicio.** La suite actual verifica fidelidad a lo declarado, con casos escritos en la propia carpeta. Verificar juicio pide casos retenidos fuera de la carpeta y comparación a ciegas. Ningún formato de la categoría lo hace.
