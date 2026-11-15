# Día 1 – Laboratorio en Mac M4 (UTM + Ubuntu)

**Fecha:** 7 de octubre de 2026
**Objetivo:** Montar un entorno seguro para practicar Linux sin tocar
mi sistema real.

---

## Conceptos base

### ¿Qué es una máquina virtual (VM)?
Es una computadora "simulada" que corre dentro de mi Mac, como un
programa más. Tiene su propio sistema operativo y es independiente:
si algo sale mal ahí dentro, mi Mac no se ve afectada. Por eso es
ideal para practicar ciberseguridad.

### ¿Qué es UTM?
Es el programa que crea y corre máquinas virtuales en Mac. Lo elegí
en vez de VirtualBox porque funciona mejor en los chips Apple (M1–M4).

### ¿Qué es ARM64 y por qué importa?
ARM64 es el tipo de arquitectura (el "idioma") del procesador.
- Los chips Intel/AMD usan **x86_64**.
- Los chips Apple (M1–M4) y los celulares usan **ARM64**.
Un sistema compilado para una arquitectura no corre en la otra. Como
mi Mac es ARM64, descargué la versión **ARM64** de Ubuntu.

### ¿Qué es Ubuntu?
Es una distribución (una versión) de Linux, el sistema operativo que
más se usa en servidores y en ciberseguridad.

---

## Qué hice (pasos)
1. Descargué e instalé UTM (mac.getutm.app).
2. Descargué la imagen ISO de Ubuntu Server para ARM.
3. En UTM: creé la VM → "Virtualize" → "Linux", asigné RAM, núcleos
   de CPU y espacio de disco, y seleccioné la ISO.
4. Arranqué la VM y seguí el instalador de Ubuntu.
5. Como Ubuntu Server no trae entorno gráfico, instalé el escritorio:
   `sudo apt update`, luego `sudo apt install ubuntu-desktop`,
   luego `sudo reboot`.

---

## Problemas y soluciones
- Al reiniciar al final de la instalación, la VM se quedó en pantalla
  negra con el cursor parpadeando. Es **normal**: cerré la VM, quité
  la ISO y la volví a encender.

## Glosario
- *VM (virtual machine)* = máquina virtual
- *ISO* = archivo que contiene un sistema operativo para instalar
- *ARM64 / x86_64* = tipos de arquitectura de procesador
- *distribución (distro)* = una versión de Linux (ej. Ubuntu)
- *sudo* = ejecutar un comando como administrador (ver nota aparte)
