
# IIC2173 - Entrega 2

## Plazo

Fecha de entrega en repositorio: 18 de octubre a las 23:59pm.
Fecha de entrega coevaluación: 20 de octubre a las 23:59pm.
Presentación: 18 de octubre a las 10:00am.

## Introducción

Ya han definido como y que quieren hacer: es momento de lanzarse al desarrollo!

En esta fase deberán entregar un prototipo funcional del juego y de *The Steam*, más la configuración de desarrollo operacional.

## Entregables

Para la segunda entrega, tanto como **grupo** y **macrogrupo**, les pediremos que realicen lo siguiente:

- Prototipo del juego/The Steam
    - No se espera grandes avances, sino que se pueda ver que existe un esqueleto simple del juego/The Steam, en algunas de sus características.

- Deploy de su aplicación
    - Deberán montar sus propios servidores.
    - Se debe utilizar servicios **IaaS**.
    - Se puede tener más de un servidor por grupo/macrogrupo. (**ojo** con el manejo de los créditos)
- Dominios
    - Cada servidor utilizado en el desarrollo su aplicación tendrá que tener un dominio TK, ML o GA asignado.
    - Los dominios TK son gratuitos, y pueden conseguirlos fácilmente en Freenom.
- Docker
    - Deben configurar sus ambientes de desarrollo con Docker, en vista a usar docker-compose, AWS ECS, EKS u otro servicio de orquestado de containers.
    - Esto se debe realizar para The Steam, ya que es un servicio web. Y los grupos que tengan servicios web también deberán tener Docker implementado. De no tener web, no será necesario.
- Continuous integration
    - Se pedirá asociar el repositorio a Travis CI/Circle CI.
    - No será necesario que se haga *deploy* automáticamente en sus servidores (debido a la dificultad), sino que se ejecuten los tests cada vez que hagan pull request a _development_.
    - Esto sólo se realizará para The Steam.
- Testing
    - Se deberán testear las funcionalidades realizadas, principalmente las interacciones.
    - El objetivo es que el CI que utilicen corra estos tests, por lo que deberían ser tests unitarios/integración.
- Requisitos no funcionales
    - Esto lo realizará solo el **grupo**.
    - Performance: El juego debe demorar máximo 2 segundos en empezar. Y menos de 1.5 segundos para el 90% de los casos. 
    - Seguridad: la mensajería entre componentes y aplicaciones debe realizarse de forma encriptada. Además, todas las contraseñas y variables de entorno **no** deben ser públicas.
    - Confiabilidad: El juego debe poder guardar los datos de la partida ante alguna caída. El sistema de puntos debe reflejar los resultados reales de las partidas.
    - Disponibilidad: En el caso de que un juego deje de funcionar o que la conexión a Steam se vea perjudicada por el internet u otro factor, se debe poder seguir utilizando el sistema. El usuario no puede saber que se cayó el sistema.
    - Escalabilidad: Se deben realizar tests de carga para las interacciones entre los juegos ya que si se desean colocar más juegos o aumenta la carga del sistema, entonces las funcionalidades no podrán fallar. 
    - Usabilidad: se debe realizar, con al menos 15 personas, pruebas de funcionalidad de las interacciones de la aplicación. Deben poder ser fácilmente usables desde el punto de vista del usuario. 


Finalmente, se les pedirá que como macrogrupo, hagan una presentación en formato PDF que incluya lo siguiente:

- Nombre del macrogrupo
- Presentacion de los avances de cada uno de los grupos.
- Demo simple de los juegos del grupo.
- Demo simple de *The Steam*.


La presentación de esta entrega se hará en horario de ayudantía, y **debe asistir al menos una persona por grupo**, haciendo así **4 personas al menos por macrogrupo**.

La presentación tendrá una duración de 10 minutos. Además, habrán 5 minutos para preguntas.

## Evaluación

Esta entrega genera dos notas, **E<sub>1 grupal</sub>** por los artefactos pedidos para el grupo y **E<sub>1 macro</sub>** por la presentacion del macrogrupo.

### Grupal

La nota grupal se calcula como: 

**E<sub>1 grupal</sub> = E<sub>1 grupo individual</sub> * 0.7 + E<sub>1 macro</sub> * 0.3**

### Individual

Segun el programa del curso, esto se evalua como:

**E<sub>1</sub> = 1 + ((E<sub>1 grupal</sub> - 1) * F<sub>g</sub>)**			

Donde F<sub>g</sub> es un factor de coevaluación asignado por el grupo que va de 0 a 1.2. Para esto se enviará un form de coevaluación donde cada integrante deberá evaluar a sus compañeros de grupo con una puntuación entre 1 y 5. 

**No podrán asignarle 5 puntos a más de un compañero, y sí lo hacen, se considerará que se entregó un máximo de 4 puntos a cada compañero**.

De no realizar la coevaluación, asumiremos que se le entregó el mismo puntaje de coevaluación a cada integrante, es decir 4 puntos.
