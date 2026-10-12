# Instalación por plataforma

> Parte del estándar .contexto/ · v1.6
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

Uní el contenido en un solo documento respetando el orden de lectura de `guia.md` (la guía primero y después los materiales de la capacidad que vas a usar). El estándar no cambia: cambia el empaque.

## Empezar a usarla

Pedile una aplicación concreta: un texto, una presentación o una propuesta visual con los materiales de tu carpeta. Comprobá que puede leer los archivos y seguir las instrucciones del formato. A partir de esa primera aplicación podés desarrollar la pieza, sumar referencias o abrir otra capacidad. `verificacion.md` ayuda a revisar datos y condiciones operativas; `auditoria.md` propone cómo ampliar la base.

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
