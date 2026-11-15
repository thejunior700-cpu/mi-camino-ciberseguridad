# Sala 4 – Fundamentos de hardware (TryHackMe)

**Fecha:** 22 de octubre de 2026
**Plataforma:** TryHackMe – reto forense "Case CB-0047"
**Bandera:** [obtenida — no se publica por buenas prácticas]

---

## De qué trató
Un reto de forense digital: reconstruí una PC de escritorio pieza por
pieza, eligiendo las 7 correctas (descartando "impostoras"),
arranqué la máquina, respondí un cuestionario de hardware y recuperé
un archivo de evidencia.

---

## Los componentes de una PC y qué hace cada uno

| Componente | Qué hace | Dónde va |
|------------|----------|----------|
| CPU (procesador) | Procesa cada instrucción. Es "el cerebro" | Socket en la placa madre |
| RAM (memoria) | Guarda datos temporales que se usan ahora. Se borra al apagar | Ranuras DIMM |
| PSU (fuente) | Convierte la electricidad del enchufe al voltaje de cada parte | Borde del chasis |
| Placa madre (motherboard) | Conecta y comunica todos los componentes entre sí | Es la base de todo |
| Almacenamiento (SSD/HDD) | Guarda archivos y el sistema de forma permanente | SSD: sobre la placa / HDD: bahía |
| GPU (tarjeta gráfica) | Genera la imagen que se ve en pantalla | Ranura PCIe x16 |
| Adaptador de red | Conecta la PC a la red / internet | Interno, parte trasera |

Las piezas "impostoras" eran de **laptop** o externas (cargador de
laptop, GPU de laptop, dongle Wi-Fi USB): no van en una PC de
escritorio.

---

## Conceptos clave aprendidos

### SSD vs HDD (almacenamiento)
- **SSD (Solid State Drive):** sin partes móviles, rápido, silencioso.
  Es el moderno. El reto pedía este.
- **HDD (Hard Disk Drive):** usa discos magnéticos giratorios, es más
  lento y antiguo. La máquina avisó "disco mecánico detectado" y pidió
  usar el más rápido (SSD).

### Qué es "arrancar" (boot)
Es el proceso de encender la máquina y cargar el sistema operativo. El
disco desde el que arranca se llama **disco de arranque**.

### Concepto de seguridad: Cold Boot
La bandera obtenida hacía referencia a "cold boot complete". Un
**cold boot attack** es una técnica forense real: la memoria RAM
retiene datos unos segundos tras apagar la máquina, y de ahí se puede
extraer información (incluso contraseñas). Por eso la evidencia se
"extrajo de la memoria".

## Glosario
- *motherboard (MOBO)* = placa madre
- *CPU* = procesador (el "cerebro")
- *RAM* = memoria temporal de trabajo (se borra al apagar)
- *PSU* = fuente de poder
- *boot / cold boot* = arrancar / arranque en frío
- *mechanical drive* = disco mecánico (HDD)
- *flag* = bandera (código que prueba que resolviste el reto)
