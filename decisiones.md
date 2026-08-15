# Decisiones del estándar

> Parte del estándar [.contexto/](README.md). El registro de qué entró, qué quedó afuera y por qué.

Cada archivo candidato se evalúa contra el criterio de admisión del README: responde una pregunta que ninguno de los existentes responde, nació de una falla observada en uso con su fecha y su caso, el ejemplo lo puede demostrar con contenido real, y su ausencia se nota en lo que la IA produce. Los cuatro, o entra como sección de un archivo existente.

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

Registrar deseo, comprensión, confusión, uso, fricción y riesgo, con su lectura y su movimiento posible.

**Pasa:** responde una pregunta que ningún archivo responde, y existe funcionando en la implementación de referencia desde el 2026-06-27.
**No pasa:** no nació de una falla observada, y su forma depende del negocio de cada sujeto, con lo cual la plantilla se convertiría en un CRM chico. Su ausencia no se nota todavía en lo que la IA produce.
**Queda:** afuera del estándar, viviendo en la operación de cada implementador. Se revisa cuando aparezca una falla concreta que lo pida.

## Resueltos como sección, no como archivo

- **Patrones de lenguaje generado por IA.** El Brand Context Protocol les da un archivo propio. Acá entraron como sección tipificada de `formas.md`, porque comparten naturaleza con el resto de las prohibiciones y separarlos hacía que se leyeran como un tema aparte.
- **Tokens de diseño en formato de máquina.** Entraron como sección de `visual.md`, con la regla de que viajen dentro de la carpeta cuando se entrega a un tercero.
- **Qué cuesta sostener cada convicción.** Idea tomada de `values.md` del Brand Context Protocol. Entró como sección de `identidad.md`.
- **Procedencia y frescura.** Entró como frontmatter de todos los archivos, sin archivo propio. Originado en una falla del 2026-08-14: un archivo derivado quedó atrás de su fuente y se operó igual que uno vigente.

## Excluido por diseño

- **Gobernanza multiagente y permisos por sección.** El modelo de este estándar es un dueño y su IA. Los permisos por asiento pertenecen a productos para equipos, y Creed resuelve bien esa tesis, que es otra.
- **Infraestructura propia.** Sincronización automática, scoring como servicio o conector propio. El estándar es una convención de archivos neutral; las herramientas que lo operan son otra capa, de cada implementador.

## Abierto

- **Herencia entre marca madre, producto y submarca.** `brand.md` lo resuelve con fusión de guardrails, donde un hijo endurece y nunca debilita. Falta decidir la forma acá: carpetas anidadas que heredan, o un campo de alcance dentro de cada archivo.
- **Descubrimiento.** Cómo se publica una carpeta en un dominio para que un agente ajeno la encuentre sin que nadie se la pase.
- **Verificación de juicio.** La suite actual verifica fidelidad a lo declarado, con casos escritos en la propia carpeta. Verificar juicio pide casos retenidos fuera de la carpeta y comparación a ciegas. Ningún formato de la categoría lo hace.
