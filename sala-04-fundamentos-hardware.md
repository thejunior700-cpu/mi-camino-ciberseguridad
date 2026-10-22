# Sala 4 – Fundamentos de hardware (TryHackMe)

**Fecha:** 22 de octubre de 2026
**Plataforma:** TryHackMe – reto forense "Case CB-0047"

## Qué hice
Reconstruí una PC de escritorio pieza por pieza en un reto de
forense digital: elegí los 7 componentes correctos (descartando
"impostores"), arranqué la máquina, respondí un cuestionario de
hardware y recuperé el archivo de evidencia.

## Los 7 componentes de una PC y su función

| Componente | Función | Dónde va |
|------------|---------|----------|
| CPU (procesador) | Procesa cada instrucción; "el cerebro" | Socket del CPU |
| RAM (memoria) | Datos temporales de uso actual; se borra al apagar | Ranuras DIMM |
| PSU (fuente) | Convierte la electricidad al voltaje de cada parte | Borde del chasis |
| Adaptador de red | Envía/recibe datos por la red | Interno, atrás |
| Panel I/O | Puertos externos: USB, HDMI, audio, Ethernet | Abertura trasera |
| GPU (tarjeta gráfica) | Genera la imagen de la pantalla | Ranura PCIe x16 |
| SSD (almacenamiento) | Guarda archivos y SO de forma permanente | Sobre la placa madre |

Todo se conecta a la **placa madre (motherboard)**, que enruta la
comunicación entre todos los componentes.

## Las piezas "impostoras" (no van en una PC de escritorio)
- Cargador de laptop, GPU de laptop → son de laptop, no de escritorio
- Dongle Wi-Fi USB → accesorio externo (ya hay adaptador de red interno)
- HDD → disco mecánico, más lento y antiguo que el SSD

## Lección clave: SSD vs HDD
- **SSD:** sin partes móviles, rápido, silencioso. El correcto aquí.
- **HDD:** discos magnéticos giratorios, más lento. La máquina avisó
  "disco mecánico detectado" y pidió usar el disco más rápido (SSD).

## Concepto de seguridad: Cold Boot
La bandera fue `THM{c0ld_b00t_c0mpl3t3}`. Un **cold boot attack** es
una técnica real: la RAM retiene datos unos segundos tras apagar la
máquina, y de ahí se puede extraer información (incluso contraseñas).
Por eso la evidencia se "extrajo de la memoria".

## Glosario
- *motherboard (MOBO)* = placa madre
- *boot / cold boot* = arrancar / arranque en frío
- *mechanical drive* = disco mecánico (HDD)
- *VPN* = red privada virtual
- *compromised* = comprometido (vulnerado)
- *flag* = bandera (código que prueba que resolviste el reto)
