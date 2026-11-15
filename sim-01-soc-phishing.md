# Simulación SOC 1 – Introducción al phishing (TryHackMe)

**Fecha:** 12 de noviembre de 2026
**Plataforma:** TryHackMe – SOC Simulator
**Resultado:** Aprobado · 100% de verdaderos positivos · 4 alertas cerradas

---

## De qué trató
Actué como analista SOC de nivel 1 en un simulador que imita el
trabajo real: me llegaban alertas a una cola, las investigaba, las
clasificaba y redactaba un informe de cada incidente. El escenario era
una campaña de phishing contra la empresa thetrydaily.thm.

---

## Conceptos base

### ¿Qué es el phishing?
Es un engaño por correo (u otro medio) donde el atacante se hace pasar
por alguien de confianza (un banco, Amazon, RR.HH.) para que la
víctima haga clic en un enlace, entregue sus datos o descargue algo
malicioso.

### TP vs FP (la clasificación más importante)
- **TP (True Positive / Verdadero Positivo):** la alerta acertó, SÍ
  había algo malicioso real.
- **FP (False Positive / Falso Positivo):** falsa alarma, era
  actividad legítima que la alerta marcó por error.

### Otras herramientas y términos
- **SIEM:** sistema que junta y muestra los registros (logs) para
  investigar.
- **Cola de alertas (alert queue):** donde esperan las alertas por revisar.
- **Escalar (escalate):** avisar a un analista más experimentado
  cuando el caso lo amerita.

---

## El flujo de trabajo del analista (lo que hice en cada alerta)
1. **Asignar** la alerta (tomar el caso como responsable).
2. **Triage:** priorizar según la gravedad.
3. **Analizar** el correo: remitente, enlace, dominio.
4. **Investigar alertas relacionadas** (ej. la del firewall).
5. **Clasificar** (TP o FP) y **redactar el informe** con la evidencia.

---

## Cómo detecté el phishing: banderas rojas (checklist)
Esto es lo más útil para recordar. Un correo es sospechoso si tiene:
1. **Dominio del remitente falso o que no coincide:**
   - RR.HH. real usaría el dominio de la empresa, no uno externo
     (ej. `hrconnex.thm` en vez de `thetrydaily.thm`).
   - Amazon real es `amazon.com`, no `amazon.biz`.
2. **Typosquatting:** dominio con una letra cambiada para parecer real
   (ej. `m1crosoftsupport.co`, con un "1" en vez de la "i").
3. **Enlaces acortados (bit.ly):** ocultan la URL real a la que te
   mandan.
4. **Urgencia y amenazas:** "acción requerida", "48 horas o se cancela".
5. **Páginas de login falsas:** para robarte usuario y contraseña.

Las 4 alertas que investigué eran phishing real → todas **TP**.

---

## Métricas que aprendí
- **Tiempo de resolución:** cuánto tardo en cerrar una alerta.
- **Dwell time (tiempo de permanencia):** cuánto vive la amenaza antes
  de que la contenga. Bajarlo es clave en defensa.

## Para mejorar (feedback del simulador)
- Identificar mejor a los responsables (rol/departamento), no solo
  listar las entidades afectadas.
- Dar más contexto de los sistemas involucrados.
- Bajar el tiempo de resolución con la práctica.

## Glosario
- *phishing* = engaño para robar datos o infectar, haciéndose pasar por alguien de confianza
- *true / false positive* = verdadero / falso positivo
- *triage* = clasificación inicial por prioridad
- *typosquatting* = registrar dominios con errores tipográficos para suplantar marcas
- *SIEM* = sistema que centraliza logs para investigar
- *dwell time* = tiempo que la amenaza estuvo activa antes de contenerla
- *escalate* = escalar a un nivel superior
- *remediation* = acciones correctivas
