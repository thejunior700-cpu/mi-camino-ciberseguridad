# Sala 5 – Tipos de computadoras (TryHackMe)

**Fecha:** 12 de noviembre de 2026
**Plataforma:** TryHackMe – Pre Security (Computer Fundamentals)
**Bandera:** THM{8_computer_types}  ·  Examen final: 5/5

## Qué hice
Completé una sala interactiva de 5 tareas sobre los distintos tipos
de computadoras: encontré computadoras ocultas, comparé enfriamiento,
probé redundancia de energía y emparejé cada máquina con su uso ideal.

## Tipos que usas de frente
| Tipo | Pantalla/teclado | Propósito |
|------|------------------|-----------|
| Laptop | Sí | Portátil, uso diario |
| Desktop | Sí | Fijo, rendimiento sostenido |
| Workstation | Sí | Precisión y fiabilidad (3D, simulaciones) |
| Server | No | Dar servicios a muchos usuarios por red |

## Computadoras "ocultas"
- **Smartphone:** computadora de bolsillo, optimizada para batería
- **Tablet:** táctil, pantalla más grande
- **IoT device:** conectado a la red, propósito único (termostato, timbre)
- **Embedded:** integrado en otro aparato (chip de cafetera, sensor de puerta)

**IoT vs Embedded:** la diferencia es la conectividad. El IoT se
conecta a una red; el embedded hace su trabajo dentro de la máquina,
muchas veces sin conexión.

## Conceptos clave aprendidos
- **Throttling:** una laptop baja su velocidad al calentarse porque
  tiene poco espacio para enfriar. El desktop, con más espacio y
  ventiladores grandes, mantiene el rendimiento.
- **Redundancia:** tener un repuesto. Un servidor con dos fuentes de
  energía sigue funcionando si una falla.
- **Punto único de fallo (single point of failure):** lo que la
  redundancia busca evitar. El servidor solo se cayó (OFFLINE) con
  las dos fuentes desconectadas.
- **Workstation:** usa ECC RAM (memoria que corrige errores) y
  drivers certificados, por eso es fiable para trabajo profesional.

## Por qué importa en seguridad
Mantener los sistemas disponibles aunque algo falle (redundancia,
evitar puntos únicos de fallo) es parte del trabajo defensivo /
Blue Team.

## Glosario
- *throttling* = reducción de velocidad por calor
- *redundancy* = redundancia (tener repuesto)
- *single point of failure* = punto único de fallo
- *uptime* = tiempo en línea / disponibilidad
- *ECC RAM* = memoria con corrección de errores
- *hub* = concentrador que coordina dispositivos
