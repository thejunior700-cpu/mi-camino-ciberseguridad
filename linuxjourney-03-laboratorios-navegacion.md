# Linux Journey – Navegación (pwd, cd, ls)

**Fecha:** 11 de octubre de 2026
**Recurso:** Linux Journey (Command Line) – módulo Grasshopper

---

## Conceptos base

### El sistema de archivos es un árbol
En Linux, todos los archivos y carpetas se organizan como un árbol
que empieza en una única carpeta raíz, representada por `/`. De ahí
cuelgan todas las demás carpetas y archivos.

### Rutas: absolutas vs. relativas
Una **ruta** es la dirección de un archivo o carpeta.
- **Ruta absoluta:** empieza en la raíz `/` y da el camino completo.
  Ej: `/home/pete/Movies`. Funciona desde donde sea que esté parado.
- **Ruta relativa:** depende de dónde estoy ahora. Ej: si estoy en
  `/home/pete`, puedo escribir solo `Movies`.

---

## Comandos

### pwd (print working directory)
Muestra en qué carpeta estoy ahora mismo. Solo informa, no me mueve.
Es como el "estás aquí" de un mapa.

    pwd
    /home/pete

### cd (change directory)
Cambia de carpeta. Atajos importantes:

| Comando | Qué hace |
|---------|----------|
| `cd carpeta` | Entra a esa carpeta |
| `cd ..` | Sube un nivel (a la carpeta padre) |
| `cd ~` o `cd` solo | Va a mi carpeta personal (home) |
| `cd -` | Vuelve a la carpeta donde estaba antes |
| `cd "Con espacios"` | Carpetas con espacios, entre comillas |

Símbolos: `.` = la carpeta actual · `..` = la carpeta de arriba (padre)

### ls (list)
Lista lo que hay dentro de una carpeta.

| Opción | Qué hace |
|--------|----------|
| `ls` | Lista archivos y carpetas |
| `ls -a` | Incluye los ocultos (empiezan con `.`) |
| `ls -l` | Formato largo: permisos, dueño, tamaño, fecha |
| `ls -lh` | Igual que -l pero con tamaños legibles (KB, MB) |
| `ls -t` | Ordena por fecha de modificación |

Las opciones (flags) se combinan: `ls -la` es lo mismo que `ls -al`.

---

## Nota para más adelante: los permisos
En `ls -l`, la primera columna (ej. `drwxr-x---`) son los **permisos**
del archivo:
- La `d` al inicio = es una carpeta (directory).
- Las letras `r`, `w`, `x` = permiso de leer (read), escribir (write)
  y ejecutar (execute).
Esto es clave en
