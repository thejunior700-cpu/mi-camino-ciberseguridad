# Linux Journey – The Shell (la consola)

**Fecha:** 9 de octubre de 2026
**Recurso:** Linux Journey (Command Line) – módulo Grasshopper

---

## Conceptos base

### Terminal vs. shell (no son lo mismo)
- **Terminal:** la ventana o aplicación donde escribo. Es como la
  "pantalla" donde tecleo.
- **Shell:** el programa que corre DENTRO de la terminal, lee lo que
  escribo, se lo pide al sistema y me muestra el resultado. El shell
  más común en Linux se llama **Bash**.

Metáfora: la terminal es el teléfono, el shell es la persona que
atiende y entiende lo que decís.

### El prompt (la línea de entrada)
Es la línea donde escribo. Muestra mi usuario, el nombre del equipo y
la carpeta actual, y termina en un símbolo que indica quién soy:
- `$` → usuario normal
- `#` → usuario **root** (el superusuario, con todos los permisos y
  todos los riesgos)

Cuando veo el símbolo, el shell está listo para recibir una orden.

---

## Cómo se escribe un comando
La estructura general es:

    comando opciones argumentos

Ejemplo: en `echo Hello World`, `echo` es el comando y `Hello World`
son los argumentos (lo que le paso para que trabaje).

### El comando echo
Muestra en pantalla el texto que le doy.

    echo Hola
    echo "Hola desde Bash"

Las **comillas** sirven para que el shell trate varias palabras como
un solo texto (si no, las separa por los espacios).

---

## Consejos clave de la terminal
- **Enter** ejecuta el comando.
- **Flecha arriba** recupera el comando anterior (no reescribir).
- **Ctrl + C** cancela un comando que se quedó trabado.
- Linux **distingue mayúsculas de minúsculas**: `Archivo` y `archivo`
  son distintos.
- **Los espacios importan:** `echo hola` no es lo mismo que `echohola`.

## Glosario
- *shell* = intérprete de comandos (ej. Bash)
- *terminal* = la ventana donde escribo
- *prompt* = la línea de entrada que espera comandos
- *root* = superusuario / administrador con todos los permisos
- *command* = comando / orden
- *case-sensitive* = distingue mayúsculas y minúsculas
