# Sala 5 – Tipos de computadoras (TryHackMe)

**Fecha:** 12 de noviembre de 2026
**Plataforma:** TryHackMe – Pre Security (Computer Fundamentals)
**Bandera:** THM{8_computer_types}  ·  Examen final: 5/5

---

## De qué trató
Una sala interactiva de 5 tareas sobre los distintos tipos de
computadoras: encontré computadoras ocultas, comparé enfriamiento,
probé redundancia de energía y emparejé cada máquina con su uso ideal.

---

## Tipos de computadoras que usás "de frente"

| Tipo | Pantalla/teclado | Para qué sirve |
|------|------------------|----------------|
| Laptop | Sí | Portátil, uso diario |
| Desktop | Sí | Fijo, rendimiento sostenido |
| Workstation | Sí | Precisión y fiabilidad (3D, simulaciones) |
| Server | No | Dar servicios a muchos usuarios por red |

## Computadoras "ocultas" (en objetos cotidianos)
- **Smartphone:** computadora de bolsillo, optimizada para batería.
- **Tablet:** táctil, con pantalla más grande.
- **IoT device:** aparato conectado a la red, con un solo propósito
  (termostato, timbre inteligente).
- **Embedded (integrado):** una computadora metida dentro de otro
  aparato (chip de una cafetera, sensor de una puerta).

**IoT vs Embedded:** la diferencia es la conectividad. El IoT se
conecta a una red para reportar o recibir datos; el embedded hace su
trabajo dentro de la máquina, muchas veces sin conexión.

---

## Conceptos clave aprendidos

### Throttling (reducción por calor)
Una laptop baja su velocidad cuando se calienta, porque tiene poco
espacio para enfriarse. Un desktop, con más espacio y ventiladores
grandes, mantiene el rendimiento. A esa "frenada por calor" se le
llama throttling.

### Redundancia y punto único de fallo
- **Redundancia:** tener un repuesto por las dudas. Un servidor con
  dos fuentes de energía sigue funcionando si una falla.
- **Punto único de fallo (single point of failure):** una parte que,
  si falla, tumba todo el sistema. La redundancia sirve justo para
  evitarlo. En la sala, el servidor solo se apagó (OFFLINE) cuando se
  desconectaron las DOS fuentes.

### ECC RAM
Memoria que **corrige errores** automáticamente. Las workstations y
servidores la usan para ser más fiables en trabajos largos y críticos.

---

## Por qué importa en seguridad
Mantener los sistemas **disponibles** aunque algo falle (redundancia,
evitar puntos únicos de fallo) es parte del trabajo defensivo / Blue
Team.

## Glosario
- *throttling* = reducción de velocidad por calor
- *redundancy* = redundancia (tener un repuesto)
- *single point of failure* = punto único de fallo
- *uptime* = tiempo que un sistema está disponible / encendido
- *ECC RAM* = memoria que corrige errores
- *IoT (Internet of Things)* = aparatos cotidianos conectados a la red
- *embedded* = computadora integrada dentro de otro aparato
