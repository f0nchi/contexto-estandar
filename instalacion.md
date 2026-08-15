# Instalación por plataforma

> Parte del estándar .contexto/ · v1.1
> Cómo cargar tu carpeta para que una IA la opere. En todas las plataformas el principio es el mismo: los archivos como conocimiento, y una instrucción que ordene leer `guia.md` primero (el bloque listo está en `system-prompt.txt`).

## ChatGPT

Creá un Proyecto (o un GPT propio). Subí los archivos de tu carpeta como archivos del proyecto y pegá el contenido de `system-prompt.txt` en las instrucciones. Cada conversación nueva dentro del proyecto arranca con tu contexto cargado.

## Claude

Creá un Proyecto y subí los archivos al conocimiento del proyecto. Pegá `system-prompt.txt` en las instrucciones personalizadas. En Claude Code, alcanza con la carpeta en el repo (ver abajo).

## Gemini

Creá un Gem. Subí los archivos como conocimiento y usá `system-prompt.txt` como instrucción del Gem.

## Cursor, Claude Code y agentes de código

Poné la carpeta `.contexto/` en la raíz del proyecto y agregá una línea en el archivo de reglas del agente (`.cursorrules`, `CLAUDE.md`, `AGENTS.md`): "Antes de trabajar conmigo, leé `.contexto/guia.md`".

## Si la plataforma acepta pocos archivos

Uní el contenido en un solo documento respetando el orden de lectura de `guia.md` (la guía primero, después restricciones y lógica, después el resto). El estándar no cambia: cambia el empaque.

## Cómo saber si quedó bien

Pedile a la IA que te presente en un párrafo. Si suena a cualquiera de tu rubro, el problema no es la instalación: es que a la carpeta le faltan casos. Y para una prueba completa, corré `verificacion.md` o la auditoría de `auditoria.md`.

## Comprobar que la carpeta no fue alterada

Una carpeta `.contexto/` viaja: se manda por mail, se sube a un proyecto de chat, se comparte con un equipo. Quien la recibe puede comprobar que llegó tal como salió, y quien la entrega puede dejar esa prueba adentro.

Para generar la huella, parado en la carpeta:

```
shasum -a 256 *.md > SHA256SUMS
```

Para comprobarla, quien la recibe corre:

```
shasum -a 256 -c SHA256SUMS
```

Cada archivo responde `OK` o `FAILED`. En Windows, `certutil -hashfile archivo.md SHA256`. En Linux, `sha256sum` con las mismas opciones.

`SHA256SUMS` se regenera cada vez que la carpeta cambia, y por eso no se firma a sí mismo: prueba que los archivos son los que el dueño dejó, no quién es el dueño. Para eso hace falta una firma criptográfica, que este estándar no define: es infraestructura de quien distribuya, y cada implementador la resuelve con sus herramientas.
