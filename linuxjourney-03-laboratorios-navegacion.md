# Linux Journey – Laboratorios de navegación

**Fecha:** 11 de octubre de 2026
**Recurso:** LabEx (laboratorios prácticos de Linux Journey)

## Laboratorio 1 – Crear estructura de directorios (mkdir + cd)
Armé la estructura de un proyecto web usando solo `mkdir` y `cd`.

Estructura creada:

    project/
    ├── frontend/
    │   ├── css/
    │   └── js/
    └── backend/
        ├── api/
        └── database/

### Comando nuevo: mkdir (make directory)
Crea carpetas. Puede crear varias a la vez separándolas con espacios.

    mkdir frontend backend

Luego entro a cada una con `cd` y creo sus subcarpetas:

    cd frontend
    mkdir css js
    cd ..

Verifico mi avance con `pwd` (dónde estoy) y `ls` (qué hay).

## Laboratorio 2 – pwd
Repaso de `pwd`: confirma mi ubicación mostrando la ruta absoluta
desde la raíz `/`. El sistema de archivos es un árbol y cada `/`
separa una rama.

## Concepto nuevo: sudo
`sudo` ejecuta un comando como superusuario (root), como pedir
permisos de administrador por un momento. Pide la contraseña y se
usa con cuidado (instalar programas, tocar el sistema). Lo veré a
fondo en la lección de Permisos.

## Glosario
- *mkdir (make directory)* = crear carpeta
- *sudo* = ejecutar como superusuario / administrador
- *nested directories* = carpetas anidadas (unas dentro de otras)
