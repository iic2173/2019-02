# IIC2173 - Proyecto semestral

## Objetivos

- Tomar los requisitos para un sistema y desarrollar arquitecturas de software y diseños de alto nivel.
- Diseñar software distribuido
- Diseñar software usando componentes COTS (commercial off-the-shelf)
- Aplicar frameworks y arquitecturas al diseñar una amplia variedad de software
- Trabajar en sub equipos intercoordinados
- Diseñar e implementar software usando tecnologías middleware

## Introducción

Los juegos multijugador son una gran forma de testear las habilidades de un arquitecto de sistemas de software. Esto se debe a la complejidad de implementación y a las recurrentes fallas de servicio que puede generar una mala implementación de patrones, conectores, entre otras cosas.

## The Game

En este asombroso proyecto, les pediremos que entreguen, por **grupo**, un juego relativamente simple, de reglas limitadas, que tendrá que responder a atributos de calidad para poder ser considerados como *arquitectónicamente eficientes*.

Algunos ejemplos de juegos (que no podrán copiar pero si derivar) son:

- [Smash TV](https://youtu.be/PRHSi4hBHSM?t=269)
- [RallyX](https://www.youtube.com/watch?v=TdLATjA5cn8)
- Doom (1993)
- Galaga
- [Achikaps](https://www.youtube.com/watch?v=P6F0qh1BiUI)
- Mario bros
- [Hoplite](https://www.youtube.com/watch?v=aB_oG-_pYog)
- [Mindustry](https://mindustrygame.github.io/) (No pueden usar nada del codigo fuente de este, ni referenciarlo)
- BBtan
- Algun juego tower defense
- etc ...

Algunos ejemplos de juegos buenísimos pero insuficientes:

- Real time chess
- Asteroids
- Pong
- Space invaders
- Damas
- Ajedrez (asumiendo que no programan el motor)
- etc ...

Algunos de estos podrían cambiar si utilizan multijugador.
Juegos sobredimensionados para este proyecto debido a sus complejas interfaces y reglas (no los vamos a restringir) serían:

- Limbo
- Spore
- Starcraft
- World of goo
- World of Warcraft
- Doom (2016)
- etc ...

Para el desarrollo de este juego podrán escoger los servidores, *frameworks* y lenguajes de programación que ustedes prefieran. Siempre y cuando cumplan con los requisitos del proyecto.

El juego debe ser desarrollado en alguno de los siguientes entornos

- C#
  - Unity 
  - UWP
  - WPF
- Python
  - Pygame
  - PyQt
  - Tk
  - Panda3d
- Javascript
- Java
- Kotlin
- C++
  - Unreal engine

Puede ser en celular, escritorio o web. Cualquier otro software que deseen utilizar debe ser permitido en las *issues*.

Aunque ofrecemos varias opciones, al haber pasado programación avanzada en algun momento, debieron usar *pyqt*, lo que es suficiente para comenzar. Eso si, a diferencia de la tarea, seremos mucho más exigentes, puesto que sera un grupo de 5-6 y todo un semestre.

Lo importante es que la lógica de juego sea expresada en código y que pueda comunicarse de alguna forma con otro software, junto con que ustedes mismos lo hayan escrito.

A la hora de evaluar sus resultados, el enfoque será en la lógica de juego implementado y que sea muy usable, no por la estética.


## The Steam

Aunque el juego que hayan realizado sea espectacular, no sirve de nada si es que no puede ser jugado por el público. Es por esto que, dada la necesidad de compartir sus ideas y puntajes con el mundo, como **macrogrupo** deben realizar una sencilla plataforma de distribución digital (algo similar a *Steam big picture*).

En ésta, se deberá poder acceder a los distintos juegos desarrollados por los grupos dentro de su macrogrupo y ser utilizados correctamente. *The Steam* debe estar en la nube y debe poder accederse desde cualquier parte.

Si el juego es web, la plataforma *The Steam* debe proveerlo directamente. En otro caso, debe proporcionar un ejecutable exe o apk unico que pueda lanzar el juego. No se aceptaran .ipa debido a que es muy dificil probarlos.

Además de la plataforma base, los juegos tienen que tener lo que llamamos "interacciones" en línea. Las interacciones son implementaciones de funcionalidades que permiten interactuar a los juegos entre si. Ejemplos de interacciones son *scoreboards* conectados, mensajeria in-game, etc.
Todas estas interacciones deben ser en tiempo real y **la plataforma debe implementar 4**.

Así, los juegos tendrán que comunicarse con *The steam* y proveerlo de información relevante para estas interacciones y que tengan efectos en los otros juegos, ya sea independientes o que tengan que ver con la lógica del otro juego.

Para todo esto, se deberán asignar 2 miembros de cada grupo como representantes en el macrogrupo. Estos deberan ocuparse de la interfaz del grupo y de hacer fluir la conversacion entre los grupos del macrogrupo

*The steam* puede hacerse en **cualquier framework web** que el macrogrupo escoja, pero debe contener un backend programado por ustedes. No se les exigira que usen alguna libreria o framework para el frontend, pero se recomienda.

## Requisitos

#### Servidor

Para hacer el *deploy* de su aplicación deberán montar sus propios servidores. Se debe utilizar **servicios IaaS**. Se puede tener más de un servidor por grupo/macrogrupo.

Cada servidor deberá tener configurdo un servicio proxy inverso con NGINX o Apache, que soporte SSL vía *Let's encrypt*.

#### Dominio

Cada servidor utilizado en el desarrollo del software tendrá que tener un dominio TK, ML o GA asignado. Los dominios TK son gratuitos, y pueden conseguirlos fácilmente en Freenom.

#### Bases de datos

Su aplicación deberá utilizar una base de datos poderosa acorde a sus necesidades(no de juguete, ej. *sqlite*). Un ejemplo de esto: *PostgreSQL* $\ge$ 11.5.
Pueden usar el free tier de Amazon RDS o Google Cloud SQL

#### Requisitos no funcionales

Se deberán elegir 3 requisitos no funcionales generales que priorizarán su software. De aquellas que escojan, se deberán realizar y completar metas y métricas objetivo.

Entre los requisitos funcionales que pueden elegir se encuentra:
- Performance
- Seguridad
- Confiabilidad
- Disponibilidad
- Escalabilidad
- Usabilidad

#### Git

Para versionar el código de su aplicación utilizarán un repositorio de *git*. Se les exigirá *"buenas prácticas"* sobre los *commits*.

Además, para coordinar el desarrollo sobre éste deben seguir la metodología de *branching* *Gitflow*. No es necesario seguirlas al pie de la letra, pero como mínimo deben hacer la diferencia entre *master*, *development* y las *branches* de funcionalidades.

#### Docker

Deben configurar sus *ambientes de desarrollo* con *Docker* ya que los correctores probarán sus aplicaciones y correrán sus tests a través de esta herramienta.

#### CI

Se les pedirá realizar Continous Integration y Continous Deployment. Les indicaremos en que consiste en la entrega apropiada.

#### Tests

Se les pedirá desarrollar tests para *The steam*. Les indicaremos en que consisten en la entrega apropiada.

#### *README .md*

Sus repositorios deben contener archivos *README .md* atingentes al desarrollo que contengan toda la información necesaria para corregir las entregas (como por ejemplo funcionalidades desarrolladas/por desarrollar, link a servidor, pasos necesarios para ejecutar la aplicación y sus tests).

## Grupos y macrogrupos

Por **grupo** se entenderá como el conjunto de 5 a 6 personas (ej. G01, G09).

Por **macrogrupo** se entenderá como el conjunto de 4 grupos. En este caso:

- Macrogrupo 1: G01, G02, G03, G04
- Macrogrupo 2: G05, G06, G07, G08
- Macrogrupo 3: G09, G10, G11, G12
- Macrogrupo 4: G13, G14, G15, G16

## Fases y entregas

El proyecto grupal tiene 4 fases y estas son

ID fase     | Publicación | Entrega | Presentación | Coevaluación | Fase
--------------| ------ | --- | --- | ---- | ---------
E<sub>1</sub> | 7 de septiembre | 23 de septiembre | 27 de septiembre | 24 de septiembre | Propuesta y diseño
E<sub>2</sub> | 24 de septiembre  | 11 de octubre |11 de octubre | 12 de octubre | Prototipo
E<sub>3</sub> | 12 de octubre    | 8 de noviembre |  8 de noviembre | 9 de noviembre | MVP
E<sub>4</sub> | 9 de noviembre   | TBA | TBA | TBA | Producto finalizado

Las presentaciones de las entregas E<sub>1</sub>, E<sub>2</sub> y E<sub>3</sub>, se realizarán en horario de ayudantía, y **debe asistir al menos una persona por grupo**, haciendo así **4 personas al menos por macrogrupo**. La E<sub>4</sub> aún no tiene fecha de entrega ni de presentación.

Para cada entrega E<sub>2</sub>, E<sub>3</sub> y E<sub>4</sub> se espera obtener un producto funcional. 

Se corregirá el último *commit* en la rama *master* de cada repositorio utilizado para el desarrollo del software.

Cada presentación tendrá una duración de entre 10 a 12 minutos. Además, habrán 5 minutos para preguntas.

## Restricciones y alcances

* Solo se permite usar las herramientas mencionadas aqui para construir su código, a menos que se especifique que una parte es libre. Pueden preguntar si algun lenguaje/framework/paquete esta permitido, abriendo una issue o preguntando en la instancia de reunion con sus ayudantes por macrogrupo (sera anunciado)


* Esta tarea debe tener codigo fresco desarrollado por el grupo y macrogrupo, y está regida por el [Código de honor de Ingeniería](https://www.ing.puc.cl/wp-content/uploads/2015/08/cdigo-de-honor.pdf). Cualquier uso de snippets o librerias debe ser referenciado debidamente. 

* Tendrán hasta 24 horas después del plazo de entrega de la fase para subir el README al repositorio.
  Entregas con atraso de más de 24 horas tendrán calificación grupal mínima (1.0).

## Evaluación

### Grupal

**E<sub>1 grupal</sub> = E<sub>1 grupo individual</sub> * 0.7 + E<sub>1 macro</sub> * 0.3**

### Extras

Existen extras para cada entrega que mejoran la nota, pero solo si funcionan. De no funcionar, éstos no aplicarían:

* Multiplayer por juego (en tiempo real): 5%


Actuan como ponderadores sobre la nota total del grupo. Ej.: Si la aplicacion tiene multiplayer y tuvieron un 5.3

 $5.3 * 1.05 = 5.7$

### Individual

**E<sub>0</sub> = 1 + ((E<sub>0 grupal</sub> - 1) * F<sub>g</sub>)**			

Donde F<sub>g</sub> es un factor de coevaluación asignado por el grupo que va de 0 a 1.2. Para esto se enviará un form de coevaluación donde cada integrante deberá evaluar a sus compañeros de grupo con una puntuación entre 0 y 5. 

**No podrán asignar a más de un compañero 5 puntos y sí lo hacen, se considerará que se entregó un máximo de 4 puntos a cada compañero**.

De no hacer la coevaluación asumiermos que le entregó el mismo puntaje de coevaluación a cada integrante, es decir 4 puntos.

NP = 0.15 * E<sub>0</sub> + 0.85 * PROMEDIO(E<sub>1</sub>,E<sub>2</sub>,E<sub>3</sub>,E<sub>4</sub>)
