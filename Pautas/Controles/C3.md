# IIC2173 - Pauta C3

---

**P1.** ¿Qué es la escalabilidad? ¿Cuáles son sus tipos (cómo se puede llevar a cabo) y las características de cada uno de éstos? **(3 puntos)** ?

**R:** La escalabilidad es un tipo de requerimiento no funcional, esta define la capacidad del software de adaptarse para alcanzar nuevos requisitos de tamaño y alcance.

* **Horizontal:** Añadir más máquinas.
* **Vertical:** Mejorar la máquina existente.

**Comentario:**

* 1 punto por definición correcta de escalabilidad.
* 0.5 por cada tipo de escalabilidad nombrado.
* 0.5 por explicación correcta del tipo de escalabilidad.


---
**P2.** ¿En qué consiste el teorema CAP? Explique en no más de 6 líneas. **(2 puntos)** ?

**R:** El teorema de CAP dice que, para un sistema de servidores distribuidos, es imposible garantizar simultáneamente la **consistencia, disponibilidad y tolerancia a la partición**.
- Si tenemos alta disponibilidad y tolerancia de partición, entonces no podemos asegurar consistencia.
- Si tenemos alta consistencia y tolerancia de partición, entonces no podemos asegurar disponibilidad.
- Si tenemos alta consistencia y disponibilidad, entonces no podemos asegurar tolerancia de partición.


**Comentario:** 

* 0.5 por cada definición
* 0.5 por explicación correcta

---

**P3.** ¿Cúal/es de las siguientes afirmaciones son correctas acerca de "Sharding"? **(2 puntos)** 

**R: Al tener menos tuplas, es más rápido indexar cada instancia de las tablas.**


**OJO:** ¿Por qué no?
> Al tener menos tuplas, es más rápido hacer todo tipo de consulta

No todo tipo de consultas, si realizamos alguna que requiera recorrer todas nuestras particiones, pues entonces es más lento que tener todo junto. Recordar que las particiones se realizan para beneficiar alguna consulta que sea recurrente en nuestra base de datos.

**Comentario:** 

* 2 puntos por alternativa correcta
* 1 punto de descuento por alternativa incorrecta


---

**P4.** Con una muy buena amiga usted quiere construir una pagina de adopción de gatitos en línea, donde las personas se registren y se les haga seguimiento. Esperan tener éxito instantáneo y cientos de clientes concurrentes. ¿Qué medidas de las siguientes son apropiadas para la capa que manejará la carga? **(2 puntos)** ?

**R:**

1. ❌ Al ser una página que transita informacion sensible (básicamente informacion de usuarios), no se puede sacrificar seguridad por una ganancia marginal en performance (para el 2019).
2. ✅ Cachear las imágenes reduce tiempos de carga y tráfico en servidores, y es difícil que la imagen misma cambie. Los e-tags hacen mas eficiente la cache.
3. ✅  Natural.
4. ❌ Habrá que replicar la información para cada uno de los servidores, lo que tiene un costo enorme en espacio y transacciones a la hora de escribir.
5. ❌ El calor y el pelo suelto que sale de los gatos obstruye el funcionamiento de los servidores, reduciendo su vida útil y tapando el flujo de aire.

**Comentario:** 

* 1 punto por respuesta correcta.
* 1 punto de descuento por alternativa incorrecta.

---

**P5.** Los CDN, content delivery networks, son intermediarios que uno puede utilizar (pagado por supuesto) para proporcionar contenido a los usuarios de forma acelerada, ofreciéndoles cierto tipo de archivos en un servidor de archivos mas cercano físicamente al usuario. ¿Como podría un CDN ayudar en el performance de una aplicación web? Menciona al menos 2 puntos clave. **(4 puntos)** ?

**R: Ver comentario** (Puede haber más respuestas correctas).

**Comentario:** 

* 2 puntos por mencionar que la aplicacion web ya no debe ocuparse de servir el contenido sino que se delega al CDN, liberando recursos.
* 2 puntos por reconocer que la cercania fisica al usuario reduce la cantidad de saltos y por lo tanto la latencia.
---
