# Cloud Computing Fundamentals (TryHackMe)

**Fecha:** 18 de noviembre de 2026
**Plataforma:** TryHackMe – Pre Security

## Qué es la nube
La computación en la nube es usar computadoras y servidores de otra
empresa a través de internet, en vez de tener los propios. Se basa en
la virtualización que ya aprendí. Esto ayuda a bajar costos y facilita
el desarrollo de las aplicaciones de empresas y negocios.

## Cómo evolucionó
Primero fueron los servidores físicos, más tarde la virtualización,
después la automatización, y finalmente la nube.

## Beneficios
- Escalabilidad
- Pagar solo por lo que usás
- Acceso global
- Alta disponibilidad
- Autoservicio bajo demanda

## Tipos de nube
- **Pública:** compartida, la usan casi todos.
- **Privada:** la usan empresas, bancos y gobiernos que necesitan más
  control y seguridad.
- **Híbrida:** una mezcla de las dos.

## Modelos de servicio (la analogía del alquiler)
- **IaaS:** como alquilar un apartamento vacío, vos ponés todo.
- **PaaS:** como un apartamento semi-amueblado, te dan la base y vos
  cargás y desarrollás las aplicaciones.
- **SaaS:** te dan todo listo para usar, como Gmail o Zoom.

## Proveedores
AWS es el líder. También están Azure (Microsoft) y Google Cloud,
entre otros.

## La parte práctica
Usé una consola tipo AWS y creé instancias EC2 (máquinas virtuales).
Los tipos de instancia:
- **t3.micro:** el más barato.
- **m5.large:** más potente y más caro.

Aprendí que **solo las máquinas encendidas cuestan**. Se pueden
apagar las que no se usan para ahorrar. En el ejercicio, con todas
encendidas el costo era 170 créditos al mes, y apagando las dos
máquinas de prueba (m5.large) bajó a 30 créditos.

## Glosario
- *cloud computing* = computación en la nube
- *public / private / hybrid cloud* = nube pública / privada / híbrida
- *IaaS / PaaS / SaaS* = modelos de servicio en la nube
- *EC2* = máquina virtual en la nube de AWS
- *instance type* = tipo de instancia (potencia/costo)
