
# IIC2173 - Entrega 2

## Plazo

Fecha de entrega en repositorio: 11 de octubre a las 23:59pm.
Fecha de entrega coevaluación: 12 de octubre a las 23:59pm.
Presentación: 11 de octubre a las 10:00am.

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
- Continuous integration
    - Se pedirá asociar el repositorio a Travis CI/Circle CI.
    - No será necesario que se haga *deploy* automáticamente en sus servidores (debido a la dificultad), sino que se ejecuten los tests cada vez que hagan pull request a _development_.
- Testing
    - Se deberán testear las funcionalidades realizadas.
    - El objetivo es que el CI que utilicen corra estos tests, por lo que deberían ser tests unitarios/integración.
- Requisitos no funcionales
    - Esto lo realizará solo el **grupo**. 
    - Dependiendo de los requisitos no funcionales que escogieron se les notificará dentro de los próximos días las métricas objetivo. 


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
