# Sala 6 – Client-Server Basics (TryHackMe)

**Fecha:** 16 de noviembre de 2026
**Plataforma:** TryHackMe – Pre Security (Network Fundamentals)

---

## De qué trató
Cómo se comunican las computadoras en internet usando el modelo
cliente-servidor, y cómo funciona el protocolo HTTP en la práctica
(inspeccionando peticiones reales con las DevTools del navegador).

---

## Conceptos base

### El modelo cliente-servidor
Es la forma en que se comunican los dispositivos en una red. Hay dos
roles:
- **Cliente:** el que PIDE algo (ej. tu navegador).
- **Servidor:** el que TIENE la información y la ENTREGA cuando se la
  piden (ej. la computadora donde está la página).

Regla clave: **el cliente siempre inicia la comunicación**, el
servidor responde.

### La analogía de la pizza (para recordarlo)
- Alice pide una pizza → el **cliente** hace una petición.
- El local prepara y entrega → el **servidor** responde.
- El idioma y las reglas del pedido → el **protocolo**.
- La puerta específica por la que entra cada tipo de pedido → el **puerto**.
- El GPS que convierte el nombre del local en su dirección → el **DNS**.

---

## Términos importantes

### Protocolo
Las reglas y el "idioma" que usan cliente y servidor para entenderse.
Define qué comandos existen, cómo se arma una petición y qué
respuesta dar a cada caso.

### Puerto (port)
Identifica un servicio específico dentro de un servidor. Un mismo
servidor puede ofrecer varios servicios, cada uno en un puerto
distinto (como puertas diferentes para distintos pedidos).

### DNS (Domain Name System)
Funciona como un GPS: convierte el nombre de un sitio (ej.
`google.com`) en la dirección real del servidor, que es su **dirección
IP**. Sin DNS tendríamos que memorizar números en vez de nombres.

### Dirección IP
El número que identifica a un equipo o servidor en la red. Es como la
dirección de una casa, pero para computadoras.

---

## HTTP y el método GET

### Qué es HTTP
HyperText Transfer Protocol: el protocolo cliente-servidor que usa la
web. Es "sin estado" (stateless): cada petición se procesa sola, el
servidor no recuerda las anteriores. Por eso los sitios usan cookies
o tokens de sesión para "recordar" que iniciaste sesión.

### El método GET
Sirve para OBTENER un recurso del servidor (una página, una imagen).
Cuando escribís una dirección en el navegador, él arma la petición GET
automáticamente.

### Lo que vi en la práctica (DevTools → Network)
Al entrar a UNA página, el navegador no hace una sola petición, hace
VARIAS (una por cada archivo que necesita):
- `/` (la página, index.html) → GET, estado 200
- `style.css` (los estilos) → GET, estado 200
- `script.js` (el código) → GET, estado 200
- `favicon.ico` (el iconito) → GET, estado 404 (no existía)

### Las cabeceras (headers)
Información extra que viaja con cada petición y respuesta:
- **Response headers** (del servidor): `Content-type` (qué tipo de
  contenido manda), `Server` (qué software usa el servidor).
- **Request headers** (del cliente): `Host` (a qué servidor le habla),
  `User-Agent` (identifica el navegador).

---

## Las partes de una URL
Ejemplo: `https://www.iamlearning.thm/contact`

| Parte | Valor | Qué es |
|-------|-------|--------|
| Esquema (scheme) | `https` | El protocolo (lo que va antes de ://) |
| Host | `www.iamlearning.thm` | El servidor (entre :// y la primera /) |
| Ruta (path) | `/contact` | El recurso pedido dentro del servidor |

---

## Por qué importa en seguridad
- Casi todos los ataques pasan por tráfico cliente-servidor (phishing,
  webs maliciosas, lo que analiza un SOC).
- Saber leer un **header** permite detectar cosas raras: un User-Agent
  falso, o un servidor que revela su versión (*information
  disclosure*).
- Saber desarmar una **URL** es clave para detectar phishing: el host
  falso es la pista (ej. `amazon.biz` vs `amazon.com`).

## Glosario
- *client / server* = cliente / servidor
- *protocol* = protocolo (reglas de comunicación)
- *port* = puerto (identifica un servicio en un servidor)
- *DNS* = sistema que traduce nombres a direcciones IP
- *IP address* = dirección que identifica un equipo en la red
- *HTTP* = protocolo de la web (cliente-servidor, sin estado)
- *GET* = método para obtener un recurso
- *header* = cabecera (info extra de cada petición/respuesta)
- *User-Agent* = identifica el navegador del cliente
- *scheme / host / path* = esquema / host / ruta de una URL
