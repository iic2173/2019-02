# IIC2173 - Entrega 0

## Fecha límite

Debe ser entregada a más tardar a las 23:59 del 6 de Septiembre. Las condiciones de entrega están explicadas más abajo.

## Objetivo

La entrega tiene por objetivo ser una introducción al trabajo con servicios en la nube. Para esto, deberán configurar un servidor básico en la nube y *deployear* una pequeña aplicación.

## Requisitos
Les daremos indicaciones de como crear un servidor en AWS y montar su aplicacion. En este deberán configurar un servicio web que implemente un chat anónimo, donde los usuarios puedan hablar con un alias temporal. Adicionalmente, el sitio deberá consultar alguna API de internet (que ustedes consideren pertinente, lo que ustedes prefieran), y mostrar los resultados en el sitio.
👀: **No es necesario que el sistema esté conectado a una base de datos**.

El servicio de chat pueden desarrollarlo con el framework que deseen, **EXCEPTO**:

* Koa/express
* Ruby on Rails
* PHP

Pueden utilizar cualquier otro que esté basado en:

* C/C++ :ok_hand:
* ASP.NET
* Python
* Javascript
* Rust
* Go
* Java
* Kotlin
* Prolog
* Brainfuck

Pueden preguntar en las *issues* si quieren usar otro lenguaje.

Cada servidor tendrá que tener un dominio TK, ML o GA asignado. Los dominios TK son gratuitos, y pueden conseguirlos fácilmente en Freenom. 

Finalmente, en el servidor deberán configurar un servicio *proxy* inverso con NGINX o Apache, que soporte SSL vía *Let's encrypt*.

## Enlaces relevantes

 * https://phoenixnap.com/kb/ssh-to-connect-to-remote-server-linux-or-windows
 * https://www.digitalocean.com/community/tags/deployment?type=tutorials
 * https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04-quickstart
 * https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/
 * https://www.freenom.com/es/index.html?lang=es
 * https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/

## Criterios de evaluación

La entrega tendrá 47 puntos. 47 puntos equivalen a un 7.0

### Requisitos funcionales

* **RF1: (10p)** Se debe poder enviar mensajes y que se registre su timestamp.
* **RF2: (8p)** Se debe poder ver los últimos 100 mensajes enviados en páginas de 5 mensajes cada una.
* **RF3: (5p)** Se debe desplegar correctamente el contenido de la API.

### Requisitos no funcionales

* **RNF1: (10p)** Debe haber un proxy inverso Nginx o Apache configurado.
* **RNF2: (5p)** El servidor debe tener un nombre de dominio .tk, .ml o .ga
* **RNF3: (8p)** El dominio debe estar asegurado por SSL.
* **RNF4: (1p)** No usar PHP.

## Método de entrega

Se abrirá un form para que entreguen el nombre de su dominio. Además, deben subir el código de su solución junto al archivo de configuracion de Nginx o Apache en el repositorio que se les asignará.
