# Linux Journey – The Shell

**Fecha:** 9 de octubre de 2026
**Recurso:** Linux Journey (Command Line) – módulo Grasshopper

## Qué aprendí

### Terminal vs. shell
- **Terminal:** la ventana o aplicación donde escribo.
- **Shell:** el programa que interpreta y ejecuta mis órdenes.
  El más común en Linux es **Bash**.

### El prompt (línea de entrada)
Muestra usuario, host y carpeta actual. Termina en un símbolo:
- `$` → usuario normal
- `#` → usuario root (superusuario: más permisos y más riesgo)

### Estructura de un comando
    comando opciones argumentos

Ejemplo: en `echo Hello World`, `echo` es el comando y
`Hello World` son los argumentos.

### Comando echo
Muestra en pantalla el texto que le paso.

    echo Hello World
    echo "Hello from Bash"

Las comillas agrupan varias palabras como un solo texto.

## Consejos clave
- Enter ejecuta el comando.
- Flecha arriba recupera el comando anterior.
- Ctrl-C cancela un comando bloqueado.
- Linux distingue mayúsculas de minúsculas (case-sensitive).
- Los espacios importan: `echo hello` ≠ `echohello`.

## Glosario
- *shell* = intérprete de comandos
- *prompt* = línea de entrada
- *root* = superusuario
- *command* = comando / orden
- *case-sensitive* = distingue mayúsculas y minúsculas
