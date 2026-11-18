# Virtualisation Basics (TryHackMe)

**Fecha:** 17 de noviembre de 2026
**Plataforma:** TryHackMe – Pre Security

## Qué aprendí
En esta sala aprendí sobre la virtualización. La virtualización es
cuando una sola computadora física hace de varias computadoras
independientes. Esto sirve para ahorrar costos y aprovechar mejor el
hardware.

Para que esto funcione existe el **hipervisor**, que es el software
que crea y maneja las máquinas virtuales. Hay dos tipos:
- **Tipo 1:** corre directo sobre el hardware, se usa para servidores.
- **Tipo 2:** corre dentro de un sistema operativo, ideal para
  aprender y probar. UTM (el que yo uso) es tipo 2.

## Máquina virtual (VM)
Una máquina virtual es una computadora virtual completa, aislada de
las demás. Corre sobre una computadora anfitriona (el host), que
puede ser tu propio ordenador (como cuando corro Ubuntu en UTM en mi
Mac) o un servidor. Aunque la uses desde tu ordenador, está separada
de él: si algo falla adentro, tu máquina real no se ve afectada.

## Contenedor
Un contenedor es parecido a una VM pero más liviano. No es una
máquina virtual completa: en vez de tener su propio sistema
operativo, comparte el núcleo (kernel) del host y corre una sola
aplicación. La herramienta más común es Docker.

## Por qué importa en ciberseguridad
El aislamiento permite analizar **malware** (software malicioso) sin
arriesgar tu máquina real. Es decir, dentro de una máquina virtual
puedo probar un archivo malicioso y ver cómo se comporta, sin que
dañe mi computadora de verdad.

## La parte práctica
Usé una app (Virtualization Manager) para gestionar un entorno
virtual:
- Reinicié una máquina virtual (Mail-SERVER) que estaba dando error,
  y se puso en marcha.
- Creé una máquina virtual nueva para el equipo de marketing,
  asignándole CPU, memoria y almacenamiento.
- Monitoreé los hosts (servidores físicos) y encontré tres
  situaciones: uno desconectado sin ninguna VM, uno en buen estado
  con varias VMs, y uno casi al 100% de uso, lo que podría traer
  errores y fallos a futuro.

## Glosario
- *virtualisation* = virtualización
- *hypervisor* = hipervisor (software que maneja las VMs)
- *VM / lab machine* = máquina virtual
- *host* = la computadora física que aloja las VMs
- *container* = contenedor (más liviano, comparte el kernel)
- *malware* = software malicioso
