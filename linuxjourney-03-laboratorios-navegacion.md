# Linux Journey – Laboratorios de navegación

**Fecha:** 11 de octubre de 2026
**Recurso:** LabEx (laboratorios prácticos de Linux Journey)

---

## Laboratorio 1 – Crear estructura de carpetas (mkdir + cd)
Practiqué creando la estructura de un proyecto web usando solo dos
comandos: `mkdir` y `cd`.

Estructura que armé:

    project/
    ├── frontend/
    │   ├── css/
    │   └── js/
    └── backend/
        ├── api/
        └── database/

### Comando nuevo: mkdir (make directory)
Crea carpetas. Puedo crear varias de una vez separándolas con espacios.

    mkdir frontend backend

Luego entro a cada una con `cd`, creo sus subcarpetas, y vuelvo atrás:

    cd frontend
    mkdir css js
    cd ..

Verifico mi avance con `pwd` (dónde estoy) y `ls` (qué hay).

### Qué son "carpetas anidadas"
Son carpetas dentro de otras carpetas (como css y js dentro de
frontend). "Anidar" = meter una cosa dentro de otra.

---

## Laboratorio 2 – pwd (repaso)
Reforcé `pwd`: confirma mi ubicación mostrando la ruta absoluta desde
la raíz `/`. Recordatorio: el sistema de archivos es un árbol, y cada
`/` separa una rama.

---

## Concepto nuevo importante: sudo
`sudo` significa "ejecutar este comando como superusuario (root)". Es
como pedir permisos de administrador por un momento.
- Se usa para cosas importantes (instalar programas, tocar el sistema).
- Pide mi contraseña antes de ejecutar.
- Hay que usarlo con cuidado, porque con root puedo romper cosas.
Lo veré a fondo en la lección de Permisos, pero conviene conocerlo.

## Glosario
- *mkdir (make directory)* = crear carpeta
- *nested directories* = carpetas anidadas (unas dentro de otras)
- *sudo* = ejecutar un comando como administrador / superusuario
- *subdirectorio* = una carpeta que está dentro de otra
