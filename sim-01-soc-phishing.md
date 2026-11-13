# Simulación SOC 1 – Introducción al phishing (TryHackMe)

**Fecha:** 12 de noviembre de 2026
**Plataforma:** TryHackMe – SOC Simulator
**Resultado:** Aprobado · 100% tasa de verdaderos positivos · 4 alertas cerradas

## Qué hice
Actué como analista SOC de nivel 1 en un simulador: monitoreé una cola
de alertas, investigué cada una, las clasifiqué y redacté informes de
incidente. Escenario de campaña de phishing a la empresa thetrydaily.thm.

## El flujo de trabajo del analista
1. **Asignar** la alerta (tomar el caso)
2. **Triage** (priorizar por gravedad)
3. **Analizar** los artefactos del correo (remitente, enlace, dominio)
4. **Investigar alertas relacionadas** (ej. la del firewall)
5. **Clasificar** (TP o FP) y **redactar el informe de caso**

## Las alertas que investigué

| ID | Qué era | Señal clave | Clasif. |
|----|---------|-------------|---------|
| 8814 | Phishing de "RR.HH." | Dominio externo (hrconnex.thm) ≠ empresa | TP |
| 8815 | Phishing de "Amazon" | Dominio falso amazon.biz + enlace bit.ly | TP |
| 8816 | Firewall bloqueó URL | Mismo enlace del phishing de Amazon | TP |
| 8817 | Phishing de "Microsoft" | Typosquatting: m1crosoftsupport.co | TP |

## Conceptos clave aprendidos
- **TP (True Positive):** la alerta acertó, hubo algo malicioso real.
- **FP (False Positive):** falsa alarma, era actividad legítima.
- **Typosquatting:** registrar dominios con errores (m1crosoft con "1"
  en vez de "i") para suplantar marcas.
- **Enlaces acortados (bit.ly):** ocultan la URL real maliciosa.
- **Dominio que no coincide:** un "RR.HH." real usaría el dominio de
  la empresa, no uno externo.
- **Escalar:** avisar a un analista senior cuando hay interacción real
  con la amenaza.
- **Dwell time (tiempo de permanencia):** cuánto vive la amenaza antes
  de contenerla. Bajarlo es clave en defensa.

## Banderas rojas del phishing (checklist)
- Dominio del remitente distinto o falso
- Enlaces acortados o que no coinciden con la marca
- Urgencia y amenazas ("acción requerida", "48 horas")
- Páginas de login falsas (robo de credenciales)
- Señuelos típicos: paquete no entregado, login sospechoso

## Para mejorar (feedback del simulador)
- Identificar mejor a los responsables (rol/departamento), no solo
  listar entidades afectadas.
- Dar más contexto de los sistemas involucrados.
- Bajar el tiempo de resolución con la práctica.

## Glosario
- *true/false positive* = verdadero/falso positivo
- *triage* = clasificación inicial por prioridad
- *typosquatting* = dominios con errores tipográficos para suplantar
- *dwell time* = tiempo de permanencia de la amenaza
- *escalate* = escalar a un nivel superior
- *remediation* = acciones correctivas
