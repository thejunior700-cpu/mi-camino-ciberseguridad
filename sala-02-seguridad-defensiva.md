# Sala 2 – Introducción a la seguridad defensiva (TryHackMe)

**Fecha:** 11 de octubre de 2026
**Plataforma:** TryHackMe – Pre Security

---

## Conceptos base

### ¿Qué es la seguridad defensiva?
Es proteger y vigilar sistemas: detectar ataques, investigarlos y
responder ANTES de que causen daño. Es lo opuesto a la seguridad
ofensiva (que ataca para encontrar fallas). En esta sala fui el
defensor; en la sala 1 había sido el atacante.

### ¿Qué es un SOC y un analista SOC?
**SOC** = Security Operations Center (centro de operaciones de
seguridad). Es el área que vigila la seguridad de una organización.
El **analista SOC** es la persona que mira los paneles de monitoreo,
distingue la actividad normal de la sospechosa, y responde a las
alertas. Es el puesto junior más común para empezar en ciberseguridad
(y es mi rol objetivo, Blue Team).

---

## El proceso que seguí (como un analista real)
1. **Detectar:** identifiqué la IP sospechosa en el panel de monitoreo.
2. **Analizar:** revisé qué buscaba el atacante → intentaba acceder a
   páginas ocultas como `/admin` (las mismas que se descubren con
   herramientas como dirb, de la sala 1).
3. **Contener:** bloqueé la IP del atacante en el firewall para frenar
   el ataque.

### ¿Qué es la contención?
En defensa, la prioridad inmediata es **detener el ataque mientras
está ocurriendo** (contención). Investigar los detalles y arreglar la
vulnerabilidad de fondo viene después.

---

## Medidas de defensa que vi
- **Bloquear IP:** corta todo acceso del atacante. Buen primer paso.
- **Rate limiting (limitación de velocidad):** limita cuántas
  conexiones se permiten en un tiempo dado. Fue útil acá porque el
  atacante accedía a muchas páginas muy rápido.
- **Actualizar reglas de seguridad:** refuerza el control de acceso a
  las páginas sensibles.

## Lección
Ataque y defensa son dos caras de lo mismo: entender cómo ataca el
adversario (sala 1) es lo que me permite detectarlo y detenerlo
(sala 2).

## Glosario
- *defensive security* = seguridad defensiva
- *SOC (Security Operations Center)* = centro de operaciones de seguridad
- *threat* = amenaza
- *firewall* = cortafuegos (filtra el tráfico de red)
- *rate limiting* = limitación de velocidad
- *containment* = contención (frenar el ataque en curso)
- *flag* = bandera (código que prueba que resolviste un reto)
- *IP* = dirección que identifica a un equipo en la red
