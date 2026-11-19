# Simulación SOC 2 – Phishing con Splunk (TryHackMe)

**Fecha:** 18 de noviembre de 2026
**Plataforma:** TryHackMe – SOC Simulator

## Qué hice
Usé Splunk (un SIEM, la herramienta que junta los logs para
investigar) y actué como analista investigando 5 alertas de una
campaña de phishing.

## Las que eran phishing real (TP)
- **Amazon:** usaba un dominio falso, `amazon.biz`, que intentaba
  imitar a `amazon.com`. La clasifiqué como verdadero positivo (TP)
  y la escalé para que el analista senior la investigara más.
- **Microsoft:** el dominio era `m1crosoftsupport.co`, un
  typosquatting: usaron un "1" en vez de la "i", y `.co` en vez de
  `.com`.
- **Alerta del firewall:** bloqueó el enlace acortado (bit.ly) del
  phishing de Amazon. Conecté los puntos: el enlace del correo de
  Amazon era el mismo que el firewall bloqueó, así que se ve el
  ataque completo.

## La lección más importante (aprendí de un error)
No todos los correos o dominios externos son phishing. Habían llegado
dos alertas de un dominio `hrconnex.thm` que parecía phishing porque
el dominio no coincidía con el de la empresa, pero en realidad eran
legítimas: un proveedor externo de recursos humanos.

Aprendí que hay que distinguir una imitación de una marca famosa
(phishing) de un proveedor legítimo. La regla del "dominio no
coincide" es para investigar, no un veredicto automático.

## Resultado
Detecté bien todas las amenazas reales.

## A mejorar
- Escribir informes más completos: dejar claro quién y qué equipo
  está involucrado.
- Usar mejor el SIEM para ver las acciones de cada equipo, y así
  detectar bien qué equipo está interactuando con un phishing.

## Glosario
- *SIEM* = herramienta que centraliza los logs para investigar (ej. Splunk)
- *TP / FP* = verdadero positivo / falso positivo
- *typosquatting* = dominio con una letra cambiada para imitar una marca
- *escalar* = pasar el caso a un analista con más experiencia
