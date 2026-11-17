# Usar una carpeta .contexto/

> Guía complementaria · v2.1 · 2026-11-17

La carpeta necesita estar al alcance de la herramienta que la va a leer. Su entrada es `guia.md`. Los permisos y los nombres de las funciones dependen de cada aplicación; consultá su documentación vigente para configurarlos.

## Leerla

Podés adjuntar los documentos pertinentes como material de un proyecto o darle acceso a la carpeta local. La instrucción opcional de `system-prompt.txt` indica por dónde entrar. Si una aplicación admite pocos archivos, podés reunirlos conservando sus títulos, estado y orden de lectura. El empaque no cambia el formato.

## Actualizarla

Leer una copia adjunta no implica poder modificar la carpeta original. Para mantenerla desde una IA, comprobá qué acceso de escritura tiene y dónde quedan los cambios. También podés editarla a mano o guardar las modificaciones que te proponga. Una ruta escrita en un documento solo indica ubicación.

Cada herramienta tiene su forma de cargar instrucciones de proyecto; el estándar no exige una aplicación ni un archivo de entrada específico para agentes.

## Ejemplo de uso

Dale a la IA la guía y los materiales de una capacidad, pedile una aplicación y comprobá si usó los hechos y criterios pertinentes. Si se actualiza la base, verificá que lo guardado represente lo que se decidió y que otra sesión pueda encontrarlo.

Para una experiencia ya preparada, [Trama](https://www.ideasaumentadas.com.ar/trama) distribuye por separado el método de trabajo, la sesión inicial y las skills de base.

## Integridad de una descarga

El repositorio distribuye `SHA256SUMS` para comprobar sus archivos. En macOS: `shasum -a 256 -c SHA256SUMS`. En Linux: `sha256sum -c SHA256SUMS`. La comprobación detecta cambios respecto de la lista; no prueba por sí sola la identidad del autor. El contenido personalizado necesita sus propias copias o versiones recuperables.
