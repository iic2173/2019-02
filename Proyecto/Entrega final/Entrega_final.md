# Entrega final - N de M

Dada la contingencia nacional, hemos dicidido reajustar la última entrega del curso, con el fin de que esté acotada a los objetivos de este y para que puedan experimentar algunas tecnologías que quizás no conozcan.

Para esta entrega pueden (y recomendamos) utilizar el código de su E0. Deberán asociarse en **grupos de 3 o 4 o 5**, y pueden utilizar la E0 que estimen conveniente.

La idea de la entrega es que puedan completar al menos 4 de los 8 desafíos que proponemos. Cada uno vale 15 décimas por lo que completar 4 es equivalente a la nota 7.0 (la nota parte desde 1.0). Si intentan un 5to desafío, lo harán por diversion, porque no lo vamos a poder revisar.

## Desafíos

#### 1) *Make my life serverless*: Agregar 3 servicios consumidos vía servicios AWS lambda (o cloud functions en gcloud)

* RNF evaluado:
    * Niveles de logro.
        * 3x **(0.5)** Por cada servicio conectado con lambda

**Tutoriales**

* ¿Qué son las funciones Lambda? [https://www.youtube.com/watch?v=eOBq__h4OJ4](https://www.youtube.com/watch?v=eOBq__h4OJ4)
* [https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html](https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html)
* [https://stackify.com/aws-lambda-with-python-a-complete-getting-started-guide/](https://stackify.com/aws-lambda-with-python-a-complete-getting-started-guide/)
* https://medium.com/@gulikholmatova/building-a-serverless-react-app-using-aws-lambda-dynamodb-and-an-api-gateway-f846696f34cd 



---


#### 2) *Screw db hacks*: Encriptar algún tipo de chat end-to-end con Vault (secreto compartido entre peers y no con el server)

* RNF evaluado: Seguridad
    * Niveles de logro
        * (1.5) Demostrar el funcionamiento final


**Tutoriales**

¿Qué es Vault? [https://www.youtube.com/watch?v=VYfl-DpZ5wM](https://www.youtube.com/watch?v=VYfl-DpZ5wM)


* [https://www.vaultproject.io/intro/getting-started/index.html](https://www.vaultproject.io/intro/getting-started/index.html)

* [https://www.linode.com/docs/applications/configuration-management/use-hashicorp-vault-for-secret-management/](https://www.linode.com/docs/applications/configuration-management/use-hashicorp-vault-for-secret-management/)



---

#### 3) *Local NSA*: Monitoreo de lo que tengan (de servers y ojalá de red)

* Niveles de logro
    * **(0.5)** Conectar los logs de aplicacion y deploy con servicios de la nube (Cloudwatch o el nativo de la cloud que se use)
    * **(1.0)** Conectar herramientas ad-hoc como Prometheus, NewRelic o algún APM

**Tutoriales** 

* [https://www.edureka.co/blog/amazon-cloudwatch-monitoring-tool/](https://www.edureka.co/blog/amazon-cloudwatch-monitoring-tool/)
* [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-tutorials.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-tutorials.html)
* [https://prometheus.io/docs/prometheus/latest/getting_started/](https://prometheus.io/docs/prometheus/latest/getting_started/)




---

#### 4) *Containers for breakfast*: Montar los n servicios de chat en K8s o docker-compose, para modo dev y para deploy.
* RNF evaluado:
    * Niveles de logro
        1. **(0.3)** Containerizar cada servicio que lleven del grupo
        2. **(0.4)** Tener una versión funcional del código en docker-compose para desarrollo.
        3. **(0.8)** Subir este código como containers a ECS, EKS o algun servicio en la nube que esten usando

**Tutoriales**

¿Qué es Docker? [https://www.youtube.com/watch?v=Q5POuMHxW-0&feature=emb_title](https://www.youtube.com/watch?v=Q5POuMHxW-0&feature=emb_title)

* [https://medium.com/@khandelwal12nidhi/docker-setup-on-aws-ec2-instance-c670ff3d5f1b](https://medium.com/@khandelwal12nidhi/docker-setup-on-aws-ec2-instance-c670ff3d5f1b)
* [https://aws.amazon.com/es/getting-started/tutorials/deploy-docker-containers/](https://aws.amazon.com/es/getting-started/tutorials/deploy-docker-containers/)
* [https://aws.amazon.com/getting-started/projects/deploy-kubernetes-app-amazon-eks/](https://aws.amazon.com/getting-started/projects/deploy-kubernetes-app-amazon-eks/)


---

 
#### 5) *Beyond Travis*: AWS codepipeline (build, deploy) para la app de la entrega 0 (*No usar travis, ni Circle CI, solo codepipeline*)
* *Pueden usar Google Deployment Manager, pero no tiene diagramas al parecer)*
* RNF evaluado: 
    * Niveles de logro:
        1. **(0.5)** Construir buildspec.yml, y tener un build exitoso.
        2. **(0.8)** Construir un appspec.yml y lograr un deploy exitoso a una instancia EC2 (o ECS o lo que usen) desde su repositorio en Github contra un push de la rama master (no usar github activites)
        3. **(0.2)** Exponer los logs del deploy a cloudwatch u otra app

**Tutoriales**

* Video con animaciones simpáticas [https://www.youtube.com/watch?v=YxcIj_SLflw](https://www.youtube.com/watch?v=YxcIj_SLflw)
* [https://aws.amazon.com/es/getting-started/tutorials/continuous-deployment-pipeline/](https://aws.amazon.com/es/getting-started/tutorials/continuous-deployment-pipeline/)
* [https://www.sumologic.com/insight/aws-codepipeline/](https://www.sumologic.com/insight/aws-codepipeline/)


---

#### 6) Implementar un load balancer con su app e integrar un CDN en la solución (En el caso de AWS, Cloudfront + Elastic Load Balancer)

* RNF evaluado: Escalabilidad y performance.
    * Niveles de logro
        1. **(0.5)** Montar la solución en un ASG (auto-scaling group)
        2. **(0.2)** Apuntar desde el load-balancer al ASG y que venga con la URL, que quede un registro del server que manejó el request
        3. **(0.3)** Log compartido a nivel del ASG 
        4. **(0.5)** Requests de assets estáticos cacheados en el CDN.

**REVISAR APP A IMPLEMENTAR**

**Tutoriales**
* ¿Qué es Elastic Load Balancing?[https://www.youtube.com/watch?v=VIgAT7vjol8](https://www.youtube.com/watch?v=VIgAT7vjol8)
* [https://learnetto.com/blog/cloudfront-s3](https://learnetto.com/blog/cloudfront-s3)
* [https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-getting-started.html](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-getting-started.html)
* [https://intellipaat.com/blog/what-is-aws-elb-load-balancer/](https://intellipaat.com/blog/what-is-aws-elb-load-balancer/)




---

#### 7) *Arquipowerpoint*: Terraform u CloudFormation 
* RNF evaluado: Consistencia y Confiabilidad.
    * Niveles de logro
        * **(1.0)** Generar el "script" (yml) para subir la infra de un servicio básico (Balanceador, ASG, db)
        * **(0.5)** Documentación asociada a los posibles errores para poder ejecutarlo sin problemas.

**Tutoriales**
* ¿Qué es AWS CloudFormation? [https://www.youtube.com/watch?v=Omppm_YUG2g](https://www.youtube.com/watch?v=Omppm_YUG2g)
* [https://aws.amazon.com/cloudformation/getting-started/](https://aws.amazon.com/cloudformation/getting-started/)

* [https://blog.gruntwork.io/an-introduction-to-terraform-f17df9c6d180](https://blog.gruntwork.io/an-introduction-to-terraform-f17df9c6d180)
* [https://learn.hashicorp.com/terraform/getting-started/install.html](https://learn.hashicorp.com/terraform/getting-started/install.html)



---

#### 8) *Mastermind*: Conectar el chat con alguno de otro grupo.

* RNF evaluado: Consistencia y Confiabilidad.
    * Niveles de logro
        * **(0.6)** Crear una mini API (online) que pueda adaptar 3 o más chats y canalizar los mensajes de la sala principal de cada chat
        * **(0.3)** Tener una API REST documentada para esto
        * **(0.6)** Que los mensajes recibidos se vean en ambas aplicaciones

**OJO:** Deben hacer este desafío en la plataforma de la nube que escogieron, sin usar firebase o algun equivalente.
* *No es necesario que funcione en tiempo real, puede ser con un refresh*

---

#### X) Propuesta

* Pueden proponer alguna feature y niveles de logro para esta. 
* Deben dividir los niveles de logro en 3, para poder evaluarlos
* Se recomienda consultar antes, ya que puede no ser aprobada y tendrán que elegir la otra que hayan escogido en el form de inscripción.


## Entrega

13 de diciembre - 23:59 para el código.
Debe estar detallado en el README.md los detalles de su implementacion y como revisarla (links a las partes abiertas de las apps)
     
## Evaluación

Reunión online con mayoría simple del grupo, la semana siguiente a la de la entrega. Será por google meet y deberá durar entre 15-20 min, con una demo sencilla de lo que hicieron (podran compartir su pantalla y mostrar lo necesario).


 
 
 

 
