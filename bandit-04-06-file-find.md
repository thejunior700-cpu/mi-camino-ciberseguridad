# Bandit (OverTheWire) – Niveles 4 a 6

**Fecha:** 17 de noviembre de 2026
**Recurso:** OverTheWire – Bandit
(No pongo las contraseñas: regla del juego. Explico el cómo.)

---

## Nivel 4 → 5
Tenía que encontrar la contraseña en la carpeta `inhere`. Dentro
había 10 archivos (`-file00` a `-file09`), pero solo uno tenía texto
legible (que se puede leer). Usé un comando que aprendí para ver de
qué tipo era cada archivo:

    file ./*

Busqué el que decía "ASCII text" (era el `-file07`), lo leí con `cat`
y copié la contraseña.

## Nivel 5 → 6
Dentro de `inhere` había muchas más carpetas y archivos. Tenía que
encontrar uno que fuera legible, de 1033 bytes y no ejecutable. Usé
el comando:

    find . -type f -size 1033c

Eso me dio la ruta del archivo, y lo leí con `cat`.

## Algo que me pasó
Escribí `cat` sin poner el archivo y la terminal se quedó esperando,
como colgada. Aprendí que no estaba colgada, estaba esperando que yo
escribiera algo, y que con **Ctrl+C** se cancela.

## Comandos que aprendí
- `file` → dice de qué tipo es un archivo (texto, datos, etc.)
- `*` → comodín, significa "todos los archivos"
- `find . -type f -size 1033c` → busca archivos por tamaño y tipo
- `Ctrl+C` → cancela un comando trabado
