# Sala 2 – Introducción a la seguridad defensiva (TryHackMe)

**Fecha:** 11 de octubre de 2026
**Plataforma:** TryHackMe – Pre Security

## Qué hice
Actué como analista defensivo ayudando a "Joe", un analista SOC
en su primer turno, a detectar y detener un ataque al banco de
práctica FakeBank. Es la contraparte de la sala anterior: antes
fui el atacante, aquí fui el defensor.

## Qué es la seguridad defensiva
Proteger y monitorear sistemas: detectar ataques, investigarlos y
responder antes de que causen daño. Es lo opuesto a la seguridad
ofensiva, que ataca los sistemas para encontrar fallas.

## El analista SOC
SOC = Security Operations Center (centro de operaciones de
seguridad). El analista vigila paneles de monitoreo, distingue la
actividad normal de la sospechosa y responde a las alertas. Es el
puesto junior más común para empezar en ciberseguridad.

## El proceso que seguí
1. **Detectar:** identifiqué la IP sospechosa (32.122.195.63) en
   el panel de monitoreo.
2. **Analizar:** revisé qué buscaba el atacante; intentaba acceder
   a páginas ocultas como `/admin` (las mismas que se descubren con
   herramientas como dirb).
3. **Contener:** bloqueé la IP del atacante en el firewall para
   frenar el ataque.

## Contención
En defensa, la prioridad inmediata es detener el ataque mientras
ocurre (contención). Investigar los detalles y arreglar la
vulnerabilidad viene después.

### Medidas que vi
- **Bloquear IP:** corta todo acceso del atacante. Buen primer paso.
- **Rate limiting:** limita cuántas conexiones se permiten en un
  tiempo dado. Útil aquí porque el atacante accedía a muchas
  páginas muy rápido.
- **Actualizar reglas de seguridad:** refuerza el control de acceso
  a las páginas sensibles.

## Lección
Ataque y defensa son dos caras de lo mismo: entender cómo ataca el
adversario (sala 1) es lo que me permite detectarlo y detenerlo
(sala 2).

## Glosario
- *defensive security* = seguridad defensiva
- *SOC (Security Operations Center)* = centro de operaciones de seguridad
- *threat* = amenaza
- *firewall* = cortafuegos
- *rate limiting* = limitación de velocidad
- *containment* = contención
- *flag* = bandera (código que confirma que resolviste el reto)
