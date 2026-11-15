# Bandit (OverTheWire) – Niveles 0 a 4

**Fecha:** 15 de noviembre de 2026
**Recurso:** OverTheWire – Bandit (overthewire.org)
**Qué es:** Un juego para aprender a usar la terminal de Linux. Cada
nivel esconde una contraseña que te da acceso al siguiente nivel.
(Las contraseñas no se publican: regla del juego. Acá explico el
CÓMO, no las claves.)

---

## Conceptos base (para entender todo lo demás)

### La terminal y el prompt
La terminal es la ventana donde escribo órdenes. El **prompt** es la
línea que espera mis comandos; termina en `$`. Cuando veo el `$`, el
sistema está listo para recibir una orden.

### SSH (conexión remota)
`ssh` me conecta a otra computadora a través de internet. No estoy
trabajando en mi Mac, sino en el servidor de Bandit.

    ssh bandit0@bandit.labs.overthewire.org -p 2220

Qué significa cada parte:
- `ssh` → el comando para conectarse
- `bandit0` → el usuario (el nivel 0)
- `@bandit.labs.overthewire.org` → la dirección del servidor
- `-p 2220` → el puerto (la "puerta" por la que entro)

Para cambiar de nivel: salgo con `exit` y me reconecto cambiando el
número de usuario (bandit1, bandit2…), usando como contraseña la que
encontré en el nivel anterior.

Nota: al escribir una contraseña en la terminal NO se ve nada en
pantalla (ni puntos ni asteriscos). Es normal, es por seguridad.

---

## Comandos aprendidos

| Comando | Qué hace |
|---------|----------|
| `ls` | Lista los archivos de la carpeta actual |
| `ls -a` | Lista TODO, incluidos los archivos ocultos |
| `cat archivo` | Muestra en pantalla el contenido de un archivo |
| `cd carpeta` | Entra a una carpeta (change directory) |
| `exit` | Cierra la sesión SSH y vuelve a mi Mac |

### Símbolos importantes
- `./` → significa "en esta carpeta actual". Sirve para leer archivos
  cuyo nombre empieza con `-`, porque así `cat` entiende que es un
  archivo y no una opción.
- `.` (al inicio de un nombre) → el archivo está **oculto**. No
  aparece con `ls`, solo con `ls -a`.
- `.` y `..` en un listado → NO son archivos: `.` es la carpeta
  actual y `..` es la carpeta de arriba (la "padre").

### La tecla Tab (autocompletar)
Si escribo el principio de un nombre y aprieto **Tab**, la terminal
completa el resto sola. Evita errores de tipeo y pone solos los `\`
de los espacios. Es la mejor herramienta contra equivocaciones.

---

## Cómo resolví cada nivel

### Nivel 0 → 1
La contraseña estaba en un archivo `readme` en mi carpeta personal.
- `ls` → vi el archivo `readme`
- `cat readme` → leí la contraseña

### Nivel 1 → 2: archivo llamado `-`
El archivo se llamaba `-` (un guion). `cat -` no funciona, porque la
terminal cree que `-` es el inicio de una **opción** (como el `-a` de
`ls -a`), no un nombre de archivo.
- Solución: `cat ./-` → el `./` le dice que es un archivo de esta
  carpeta.

### Nivel 2 → 3: nombre con espacios
El archivo tenía espacios en el nombre. `cat spaces in this filename`
falla, porque la terminal separa por espacios y cree que son 4
archivos distintos.
- Solución: comillas para agrupar el nombre completo →
  `cat "spaces in this filename"`

### Nivel 3 → 4: espacios + guiones juntos
El archivo se llamaba `--spaces in this filename--` (guiones al
inicio Y espacios). Combiné los dos trucos:
- `cat "./--spaces in this filename--"`
  (`./` por los guiones, comillas por los espacios)

### Nivel 4 → 5: archivo oculto
La contraseña estaba en un archivo oculto dentro de la carpeta
`inhere`.
- `cd inhere` → entré a la carpeta
- `ls -a` → vi el archivo oculto `...Hiding-From-You`
- `cat "./...Hiding-From-You"` → leí la contraseña

---

## Lecciones clave
- La terminal es **literal y exacta**: una sola letra mal escrita da
  el error "No such file or directory". Por eso conviene usar Tab.
- Los nombres de archivo "raros" (guiones, espacios, ocultos) se
  manejan con `./`, comillas y `ls -a`.
- Cada nivel combina lo aprendido en los anteriores.

## Glosario
- *ssh* = conexión segura a una computadora remota
- *prompt* = la línea que espera comandos (termina en `$`)
- *port (puerto)* = la "puerta" por la que entra la conexión
- *hidden file (archivo oculto)* = empieza con `.`, se ve con `ls -a`
- *parent directory (`..`)* = la carpeta de arriba
- *"No such file or directory"* = no existe ese archivo (suele ser un
  error de tipeo o un nombre mal escrito)
