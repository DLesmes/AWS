# Notas de clase

## Razones para usar la nube
  
  * Las Pymes mejoran su economía y costos después de adoptar la nube.
  * Es una de las diez habilidades mejor pagadas en la actualidad.
  * **Almacenamiento y acceso a la información:** Cloud almacena grandes cantidades de información hasta hexabytes, puedes acceder a ella en cualquier lugar del mundo y brinda seguridad de calidad para la misma.
  * **Escalable y flexible:** Las aplicaciones pueden escalar de pocos a muchos más usuarios de forma flexible y soporta las altas demandas y, el cloud permitirá crecer basado en las necesidades de las empresas
  * **Agiliad:** En poco tiempo puedes crear una aplicación y automatizar el despliegue y servicios lo que te permite enfocarte en la aplicación y su desarrollo.
  * **Reducción de costos:** Una de las grandes ventajas del Cloud es que los costos se generan de acuerdo a las necesidades ''Pago por demanda''
  * **Innovación e Inteligencia Artificial:** Puedes acceder a servicios de realidad aumentada o detección de fraudes. Los proveedores de Cloud ya ofrecen servicios para aplicar la IA, Machine Learning o DataScience
  * **Despliegue global en minutos** La posibilidad de implementar aplicaciones y recursos en múltiples regiones del mundo de manera rápida y sencilla.
  * **Catálogo de servicios:** Acceso a una amplia variedad de servicios preconfigurados, como bases de datos, análisis y machine learning, lo que acelera el desarrollo y ahorra tiempo.

## Definiciones

### Servidores:
Un servidor es una máquina (física o virtual) que proporciona recursos, datos, servicios o programas a otros equipos, conocidos como clientes, a través de una red. En la computación en la nube, los servidores virtuales (instancias) son muy comunes

#### Tipos de Servidores en la Nube
  * Servidores Físicos: Máquinas físicas dedicadas a un solo usuario o empresa. Ejemplo: Bare Metal Servers en IBM Cloud.
  * Servidores Virtuales (VMs): Máquinas virtuales que funcionan sobre un hipervisor, permitiendo múltiples instancias en un solo servidor físico. Ejemplo: Amazon EC2, Azure VMs.
  * Servidores de Contenedores: Utilizan tecnologías como Docker y Kubernetes para ejecutar aplicaciones en contenedores aislados pero en un solo sistema operativo. Ejemplo: Google Kubernetes Engine (GKE)
    
#### Características Clave
* Escalabilidad: Capacidad de aumentar o disminuir recursos según las necesidades
* Elasticidad: Ajuste automático de recursos en respuesta a la demanda
* Alta Disponibilidad: Mecanismos para asegurar que los servicios estén disponibles casi todo el tiempo
* Seguridad: Medidas para proteger datos y aplicaciones

### Almacenamiento
El almacenamiento en la nube se refiere a la capacidad de guardar datos en una infraestructura gestionada por un proveedor de servicios en la nube. Los datos pueden ser accesibles desde cualquier lugar a través de internet

1. Almacenamiento por objetos: Divide los datos en partes distribuidas en el hardware. Cada unidad se llama objeto. (archivos, imágenes, archivos estáticos. No es para instalación de aplicaciones)
2. Almacenamiento por Archivos: Los datos son guardados como una pieza de información dentro de una carpeta. (Almacenamiento que debe ser compartido por múltiples servidores)
3. Almacenamiento por Bloque: Divide la información en bloques. Tiene un identificador único. Permite que se coloquen los datos más pequeños donde sea más conveniente. (Disco duro del servidor virtual en la nube)

### Bases de Datos
Las bases de datos son sistemas de back-end importantes que se utilizan para almacenar datos para cualquier tipo de aplicación, ya sea una aplicación móvil pequeña o una aplicación empresarial con requisitos de escala de Internet y en tiempo real

### Infraestructura como código
Permite gestionar y desplegar la infraestructura en un proveedor de servicios de nube a través de código, en vez de hacerlo por procesos manuales. El servidor que vamos a desplegar con su almacenamiento base de datos para PlatziWalet lo vamos a construir a través de código. La infraestructura la debemos pensar como código. Podemos re-utilizarla (templates)

### Función
Es un entorno de ejecución SERVERLESS para ejecutar código sin la necesidad de administrar un servidor. EL CLOUD PROVIDE se encarga de la administración y nos provee la función. AWS (lambda functions), AZURE (azure functions), GOOGLE CLOUD (cloud function). Aprender a desarrollar basado en funciones. La función siempre está dormida hasta que un evento la dispara. Evento: suben foto usuario, entonces función minimiza foto

### Docker Container
contenedor ejecutable, independiente que tiene todo lo necesario para ejecutar una aplicación

### Microservicio
Un concepto en el cual una aplicación se construye como una serie de pequeños servicios. Ejemplo: microservicio de pagos. Este microservicio de “pagos” se tiene que conectar con otro microservicio de “consulta del saldo”. Microservicios de PlatziWalet: pagos y cobros (pago a personas), formulario y promoción (suscripciones y pagos), generar y escanear (código QR), recarga y retiro (retiro y consignación)

### On-premises
Se refiere a la ubicación física de recursos informáticos, como servidores, sistemas de almacenamiento y redes, que se encuentran y operan dentro de las instalaciones de una organización. En otras palabras, cuando una empresa o entidad tiene una infraestructura informática "on-premises", significa que todos sus recursos y sistemas de TI están alojados en su propio entorno físico, como sus oficinas, centros de datos privados o instalaciones locales

En contraste, la nube y los servicios en la nube ofrecen alternativas en las que las organizaciones pueden aprovechar recursos informáticos a través de proveedores de servicios en la nube, como Amazon Web Services (AWS), Microsoft Azure o Google Cloud Platform. Estos proveedores ofrecen servicios que permiten a las organizaciones alquilar recursos informáticos de manera flexible y escalable, sin la necesidad de gestionar la infraestructura física

### Cloud Computing (Nube)

Es la entrega por demanda de infraestructura y todo tipo de servicios de aplicación vía internet

### Infraestructura Global
Todos los elementos que puede ofrecer el proveedor de servicios de nube distribuido a nivel mundial de Regiones y Zonas.
Servidores conectados a nivel global para desplegar aplicaciones (internet, última tecnología, hardware, etc). Infraestructura distribuida por todo el planeta tierra (AWS, AZURE, GCP google cloud platform).

### Región
Ubicación física donde se agrupan centros de datos. Están distribuidas en todo el mundo para prestar una cobertura Global del proveedor de servicios de nube.
Criterios para seleccionar una región
* LATENCIA (buscar mayor velocidad de respuesta),
* PRECIO (varía entre países),
* CATÁLOGO DE SERVICIOS (para el mismo CLOUD PROVIDER puede variar entre regiones).
  
### Zona de disponibilidad (AZ)
Es uno o más centros de datos. Con su propia energía, redes y conectividad redundante dentro de una región. Están interconectadas entre ellas con redes de alto ancho de banda y baja latencia. Una REGIÓN puede tener varias ZONAS de DISPONIBILIDAD (AZ). Las AZ están completamente independientes y aisladas entre ellas. Si se cae una zona no tiene que incidir en las otras.

### Balanceador de cargas
Distribuye el tráfico de requests entre AZ dentro de una misma región. El diseño de la APP tiene que ser tal que pueda correr en múltiples zonas. Multizona. Por el balanceador de cargas. De esta manera si se cae una AZ no se va a caer la APP. Con esta característica la APP tiene ALTA DISPONIBILIDAD.

### Tipos de nube
* **Nube Privada:** Una nube privada es una infraestructura de nube que está dedicada exclusivamente a una organización. Puede estar alojada en las propias instalaciones de la organización o en un entorno de centro de datos gestionado por un tercero. La nube privada ofrece mayor control y personalización, pero también requiere una inversión y administración más significativas por parte de la organización
* **Nube Pública:** La nube pública se refiere a servicios en la nube ofrecidos por proveedores externos y accesibles a través de Internet. En este modelo, los recursos y servicios se comparten entre múltiples clientes. Los ejemplos incluyen Amazon Web Services (AWS), Microsoft Azure y Google Cloud Platform. La nube pública ofrece escalabilidad, flexibilidad y menores costos iniciales, pero implica compartir recursos con otros usuarios
* **Nube Híbrida:** Una nube híbrida combina elementos de nubes privadas y públicas. Permite a una organización mantener algunas aplicaciones y datos en su infraestructura privada y, al mismo tiempo, aprovechar la nube pública para cargas de trabajo específicas. La nube híbrida ofrece flexibilidad y la capacidad de aprovechar lo mejor de ambos mundos, pero también requiere una gestión cuidadosa de la integración y la seguridad
* **Multinube:** La estrategia de multinube implica el uso simultáneo de múltiples proveedores de nube pública para alojar diferentes aplicaciones, servicios o componentes de una solución. Puede usarse para evitar el bloqueo de proveedor, aprovechar las fortalezas específicas de diferentes proveedores y garantizar la redundancia en caso de problemas con un proveedor
* **Multinube hibrida** 2 nubes públicas + 1 nube privada. Ej: PlatziWallet corre en AWS, pero tenemos la parte de procesamiento de datos y analítica en GCP. Todos los eventos que genera PlatziWallet los enviamos a GCP. Pero la APP tiene que consumir una DB que está en on-premise en una nube privada

## ¿Cuáles son los diferenciadores en la implementación entre Cloud computing y On premise?

* Modelo de costos: Modelo basado en demanda. Cambiar CAPEX por OPEX.
  * ON-PREMISES (CAPEX): costos (servidor, lugar, cable de red, aire acondicionado, ups para alimentación contínua). 10000 dólares + 2 meses para instalar
  * NUBE (OPEX): en 10 minutos luego de logueado, empiezas a pagar los costos por demanda (lo que me cobran por segundo). Costo más operativo
* Modelo de entrega y despliegue: Automatización, y creación de ambientes. Cambia la forma de trabajar. Automatización (Roles DevOps, crear Pipelines para automatizar el despliegue de aplicaciones e infraestructura). En la NUBE se pueden crear ambientes muy rápido. Para una APP se necesita una ambiente de desarrollo, uno de pruebas y uno de producción, para cada FEATURE que agregamos a la APP. Cambia el despliegue de FEATURES, SERVICIOS e INFRAESTRUCTURA
* Patrones nativos de nube: Tomar ventaja de los patrones en la nube (cloud native). Pensar en MODO NUBE. Definiciones de cómo utilizar los SERVICIOS orientados a mejores prácticas
* Escalabilidad y resiliencia: Recuperación antes fallas, utilizar zonas y regiones. Puedo tener una copia de PlatziWallet en cualquier parte del mundo (resiliencia)
* Tecnologías disruptivas: (disponibles en la NUBE, al alcance de la mano en unos minutos): AI, Data, Robots, satélites, automatización
* Modelos de seguridad compartida: Responsabilidad del usuario y proveedor de servicios Cloud¿ Que es responsabilidad del proveedor de nube y que es nuestra? Ej: responsabilidad nuestra (pusimos una clave muy fácil y se abrió el puerto 22 a todo el mundo). Responsabilidad del cloud provider (que el servidor funcione)

## **Cloud Native:** 
Construir y ejecutar una aplicación tomando todas las ventajas de Cloud Computing. La aplicación está diseñada para utilizar la escalabilidad, elasticidad, seguridad y flexibilidad del proveedor de servicios Cloud
### CLOUD NATIVE vs. APP TRADICIONALES

* **Sistema operativo:** En CLOUD NATIVE el sistema operativo pasa a un segundo plano. Ej: desplegamos la APP en SERVERLESS (la responsabilidad pasa a el Cloud Provider). En ON-PREMISES tenemos dependencia del sistema operativo (Windows Server, Linux, Redhat, etc).
* **Desarrollo:** ON-PREMISES (Waterfall development). CLOUD NATIVE (Continuous delivery) pensamos la aplicación para que sea automatizada: su despliegue, su servicios, sus nuevas features, etc. Esto nos da mucha AGILIDAD.
* **Escalabilidad:** ON-PREMISES (manual) ampliamos los recursos en el datacenter. CLOUD NATIVE (automática) utilizando serverless, contenedores, etc.
* **Capacidad:** ON-PREMISES (limitada), sobre aprovisionada(compre 10 servidores y estoy usando 2). CLOUD NATIVE (muy grande) el consumo y el costo es sobre lo utilizando.
* **INMUTABILIDAD y PREDECIBLE:** CLOUD NATIVE es inmutable porque es elástica ante picos de demanda y si tengo un error: fácilmente puedo desplegar el servicio por completo. El ON-PREMISES no tiene esa ventaja.

### CLOUD NATIVE COMPUTING FOUNDATION (CNCF):
Es una fundación de software open-source que promueve la adopción de Cloud Native Computing. Algunos proyectos (que podemos usar en CLOUD NATIVE): 
* ARGO: se utiliza para hacer despliegue de imágenes en Cluster de Kubernetes
* ETCD y KUBERNETES son vitales para desplegar cualquier aplicación cotenedrizada y orquestarla.
* FLUENTD y PROMETHEUS para toda la parte de observabilidad, monitoreo, trazas.
* PROMETHEUS se utiliza para las DB de series de tiempo.
* HELM: nos ayuda a desplegar y automatizar despliegues de aplicaciones dentro de KUBERNETES

### Beneficios de una app Cloud Native

* **Independencia:** cada aplicación es totalmente independiente de las otras
* **Resiliencia:** Puede soportar una caída de infraestructura
* **Estandarización:** Para interoperabilidad (con otros proveedores o con un on-premises, por ejemplo) y portabilidad (que se pueda mudar a otro cloud provider) de nuestra aplicación, están basadas en OPEN-SOURCE
* **Agilidad:** Flexibilidad en sus despliegues y usualmente más pequeñas (de forma RÁPIDA)
* **Automatización:** Utilización de prácticas DevOps para despliegues
1. Automatizar el despliegue de la infraestructura (TerraForm) pipelines
2. Pipelines para automatizar el despliegue de la APP en la APPSTORE y PLAY STORE
3. Automatizar el despliegue de imágenes en las funciones y los contenedores
4. Pipelines para el backend de nuestra aplicación
5. 0 Downtime: Utilizando las ventajas de la nube la hago siempre operativa a pesar de los despliegues que haga, de las nuevas features y servicios, o de los cambios que haga sobre la misma. Esto marca ventajas en el mercado.

### SERVERLESS (sin servidor)
Es la idea de que se puede ejecutar una aplicación basada en servidor sin la necesidad de administrar un servidor. Los CLOUD PROVIDER tienen servicios SERVERLESS.
El cloud provider administra el sistema operativo (parcheo, administración, escalabilidad del SO) y el usuario se enfoca en su aplicación. 
El cloud provider le da al usuario una FUNCIÓN y un CONTENEDOR SERVERLESS. El usuario pone la aplicación en el CONTENEDOR en esa FUNCIÓN.

#### RETOS de SERVERLESS:

* ESCALABILIDAD: es muy grande pero está limitada por las cuotas y los límites que pone el cloud provider. Por ejemplo la FUNCIÓN puede tener un límite de concurrencia (ej: 1000 ejecuciones concurrentes por segundo). Estos límites se pueden ampliar a través de una solicitud al cloud provider por medio de un ticket de ampliación de límites. El costo tiene que ver con estos límites.
* SEGURIDAD: el usuario se enfoca en proteger el código que publica en la función (comunicación de cifrado en tránsito). El usuario no se preocupa de la seguridad del servidor.
*FIABILIDAD: El cloud provider se compromete con una niveles de disponibilidad por arriba del 99 % (los servicios que tienen que ver con la fiabilidad y alta disponibilidad tienen un SLA muy alto).
* PAGO POR USO: por el tiempo de ejecución y la cantidad de memoria que uso para una ejecución. Ej: una FUNCIÓN se demora 200 milisegundos en tomar una imagen y convertirla en miniatura. El precio se calcula por ejecución, por consumo, cantidad de peticiones, tiempo de ejecución y cantidad de tráfico.
* AHORRO de TIEMPO y DINERO: ej: on-premises a serverless. No hay ocupación en administrar o instalar servidores. MEJORA la PRODUCTIVIDAD del DESARROLLADOR: porque los entornos actualmente en nube, los servicios, la forma de testearlos localmente, la forma de automatizar su despliegue y de probarlos es muy fácil. La agilidad para desplegar un servicio por medio de una función, teniendo el código, va a ser muy rápida (10 o 15 minutos).
* COLD START (tiempo de inicio frío): tiempo para que una FUNCIÓN se “despierte”. Hay que esperar unos 2 o 3 segundos en su primera ejecución. Esto puede afectar a algunas arquitecturas cuando no se tolera ese tiempo de latencia.
* TIEMPO de CÓMPUTO: Ejemplo. Hay FUNCIONES que su tiempo máximo de vida es 15 minutos y necesitamos un tiempo de ejecución de 30 minutos. FUNCIÓN limitada por un timeout.
* CONECTIVIDAD: Ejemplo. Consumo de direcciones IP que hace una función dentro de una capa de red. Si es alto hay que evaluar la utilidad que tiene esa función dentro de la capa. Pues es aconsejable que esa función no se ubique dentro de una VPC o una Virtual Private Cloud dentro de la red. Sino que se ejecute fuera de ella para tener más flexibilidad.
* VENDOR LOCK-IN: si queremos migrar una aplicación de AZURE a AWS lo más probable es que la tengamos que hacer de nuevo.

### Componentes de una arquitectura Serverless
-> Streams:
  * Son una secuencia de eventos, mensajes o datos que pueden ser procesados una vez ocurren, los cuales pueden ser distribuidos a múltiples consumidores.
  * Abundan en los proyectos donde la palabra clave es “data” o “real-time”.
  * Real-time:
    * es cuando se puede utilizar un evento o una acción que se acabó de generar hace poco.
    * Los streams tienen la capacidad de recibir muchísimos eventos en paralelo (millones) y se los puede enviar a un dashboard para que los grafique y lo pueda ver un equipo de marketing, por ejemplo.
    * En los cloud provider estos streams son servicios completamente serverless.
    * El streams tiene que tener la capacidad de recibir esos millones de eventos y enviarselo a un consumidor en tiempo real.

-> Colas
  * Son un método para retrasar el trabajo, utilizadas para desacoplar componentes de un sistema.
  * Ejemplo: cola para el cajero del banco.
  * Las colas se ubican para no saturar a un componente de la arquitectura.
  * Ejemplo: miles de usuarios piden un certificado a la APP, la cola en cola estas solicitudes y la aplicación lo va procesando a medida que pueda. De esta manera la APP nunca se cae.

-> Bucket
  * Es una estructura donde se puede almacenar una colección de OBJETOS.
  * Estos objetos se pueden consultar.
  * Su costo se basa en la cantidad de solicitudes y espacio utilizado.

-> Almacenamiento por objetos.
  * Un objeto puede ser la foto de cada usuario de la APP.
    
-> API
  * Es una abreviatura de APPLICATION PROGRAMMING INTERFACES, son mecanismos que permiten a dos componentes de software comunicarse entre sí, mediante un conjunto de definiciones y protocolos.
  * API REST, API HTTPS, API WebSocket, API GraphQL y todos son servicios serveless.
  * La API es la puerta de entrada a nuestra aplicación.
    
-> Datastore
  * Es una base NoSQL creada para proporcionar autoescalamiento, alto rendimiento y facilidad para el desarrollo de aplicaciones.
  * No SQL: llave valor, de memoria, por grafos y documentales.
    
-> Identity Services
  * Son servicios en la nube que ayudan a implementar la administración de acceso e identidad de los usuarios a nuestras aplicaciones web o móviles.
  * Servicios para hacer autenticación y autorización.
  * Ejemplo para PlatziWallet: yo puedo registrarme como usuario (autenticación) pero hasta que no registre una tarjeta de crédito no voy a poder realizar un pago (autenticación).
    
-> Motor de consultas
  * Es un motor de consulta SQL que pueden consultar data estructurada, semiestructurada y no estructurada de diferentes fuentes de datos.
  * Ej: PRESTO (Open Source).
  * Query a múltiples fuentes, centralizadas y el costo es por la cantidad de data escaneada.
  * A datos que tengamos en almacenamiento por objetos, a DB no relacionales y relacionales.
    
-> Balanceadores de carga
* Componente que distribuye el tráfico entre varios destinos, puede ser a nivel de aplicación, red o transporte.
* Recibe los requests y los distribuye entre las zonas de disponibilidad.
* El balanceador de aplicaciones es el que va ser nuestro foco, porque va a trabajar en capa 7 del modelo OCI, es decir, va a balancear a nivel de HTTP y HTTPS.
* El balanceador de red se enfoca en las capas 3 y 4 del modelo OCI, es decir, en balancear tráfico IP, tráfico UDP y tráfico TCP.

-> Summary
  * Funciones (Functions): Pequeños fragmentos de código que se ejecutan en respuesta a eventos específicos.
  * Eventos (Events): Desencadenantes que inician la ejecución de funciones, como solicitudes HTTP, cambios en bases de datos o mensajes en colas.
  * Plataforma Serverless: El proveedor de servicios que ofrece la infraestructura subyacente, como AWS Lambda, Azure Functions o Google Cloud Functions.
  * Almacenamiento de Datos: Bases de datos, sistemas de archivos, almacenes de objetos u otros sistemas de almacenamiento utilizados por las funciones.
  * API Gateway: Un componente que permite exponer las funciones como servicios web o API RESTful para interactuar con aplicaciones externas.
  * Colas de Mensajes (Message Queues): Utilizadas para la comunicación asíncrona y la gestión de eventos entre funciones.
  * Gestión de Identidad y Acceso: Servicios que garantizan la seguridad y la autenticación de las funciones y las aplicaciones.
  * Monitorización y Registro (Monitoring and Logging): Herramientas y servicios que permiten rastrear y analizar el rendimiento y el comportamiento de las funciones.
  * Automatización de Despliegue (Deployment Automation): Herramientas que facilitan la implementación y actualización de funciones de manera eficiente.
  * Gestión de Recursos y Escalabilidad Automática: Componentes que administran los recursos subyacentes y escalan automáticamente según la demanda.
  * Reglas y Orquestación: La capacidad de definir reglas de negocio y orquestar múltiples funciones para resolver problemas más complejos.

## Lock-ins (bloqueos/restricciones/encierros)

### Vendor Lock-in (Encierro del proveedor): 
Depender en gran medida de un proveedor específico para servicios o soluciones, lo que dificulta cambiar a otro proveedor.
  * Ejemplo: Utilizar herramientas y servicios de Amazon Web Services (AWS) exclusivamente, lo que hace que la migración a otro proveedor sea complicada debido a la dependencia de las características y servicios de AWS.
    
### Product Lock-in (Encierro del producto): 
Estar atado a un producto o software particular, lo que dificulta cambiar a otro producto.
  * Ejemplo: Utilizar una suite de productividad específica que requiere un proceso complicado para migrar a otra suite debido a las diferencias en formatos y características.
    
### Version Lock-in (Encierro de versión):
Depender de una versión específica de un producto, lo que dificulta actualizar o cambiar debido a incompatibilidades.
  * Ejemplo: Utilizar una versión más antigua de una base de datos que no es compatible con las aplicaciones modernas, lo que restringe la migración sin una actualización costosa.

### Architecture Lock-in (Encierro de arquitectura): 
Diseñar una arquitectura de manera que sea difícil cambiar debido a las dependencias profundas en componentes específicos.
  * Ejemplo: Diseñar una aplicación con dependencia en una tecnología de base de datos propietaria, lo que hace que sea difícil migrar a una base de datos diferente sin un rediseño importante.

###  Platform Lock-in (Encierro de plataforma):
Quedar atrapado en una plataforma específica que dificulta la portabilidad de aplicaciones y servicios.
  * Ejemplo: Elegir una plataforma de desarrollo que solo es compatible con un proveedor de nube, lo que hace que la migración a otro proveedor sea desafiante.

### Skills Lock-in (Encierro de habilidades):
Tener personal con habilidades especializadas en una tecnología o plataforma específica, lo que dificulta cambiar a algo diferente.
  * Ejemplo: Contar con personal altamente capacitado en una plataforma de análisis de datos específica, lo que hace que migrar a otra plataforma sea costoso debido a la necesidad de reentrenamiento.

### Legal Lock-in (Encierro legal): 
Estar limitado por acuerdos contractuales que dificultan cambiar de proveedor o producto.
  * Ejemplo: Tener contratos a largo plazo con un proveedor de servicios en la nube, lo que hace que la transición a otro proveedor sea complicada debido a las restricciones contractuales.

### Mental Lock-in (Encierro mental):
Permanecer apegado a una tecnología o enfoque familiar, incluso cuando hay mejores alternativas disponibles.
  * Ejemplo: Rechazar la adopción de nuevas tecnologías en una empresa debido a la resistencia al cambio, a pesar de que esas tecnologías podrían mejorar la eficiencia.

## MultiCloud

Utilizar más de un proveedor de servicios de nube pública para desplegar una aplicación, plataforma o sistema. Ejemplo: PlatziWallet corriendo en AWS teniendo servicios en GCP. Hay empresas que son multi nube. 

### Estrategias de multi nube
(que puede definir que despliegue determinada parte de la aplicación en la nube A o B):

* ARBITRARIO: no es una decisión técnica. Puede ser por un convenio ó MSA con el Cloud Provider, decisión de negocios, skills lock-in (los trabajadores saben X plataforma), legal lock-in (contrato por varios años con el CP).
* ELECCIÓN: seleccionar lo mejor de los mundos que se acomode a nuestro caso de uso. Mirar pros y contra de los CP realizando un estudio.
Ejemplo: Backend corre en AWS (Kubernetes) y DevOps corre en Azure (despliegue). Estoy tomando lo mejor de los mundos. Puedo tener Vendor Lock-in porque si Azure DevOps lo quiero llevar a AWS tengo que rehacerlo todo prácticamente. Por otro lado, los trabajadores van a tener que saber de AWS y de Azure.
* AGNÓSTICO: que los servicios de la aplicación puedan ser desplegados fácilmente en todos los Cloud Provider. Ejemplo: desplegar una aplicación usando Open Source en Kubernetes en AWS y hago su réplica en Kubernetes en Azure. Al ser todo Kubernetes y Open Source puedo replicarlo más fácil. La limitación Lock-in puede estar dada por los productos específicos de Open Source.
* PARALELO: Si se me cae una nube que entre otra. Es muy difícil de implementar porque tiene una complejidad técnica muy alta. Porque necesitas personal con conocimiento muy alto en 2 nubes. Funciona como un DRP (disaster recovery). Para esto las empresas tienen que definir el RTO y el RPO.
* SEGMENTADO: Ejemplo: todo nuestro Backend va a correr en Azure pero toda la parte de Data, Analítica y Machine Learning va a correr en GCP. Segmentando cargas de trabajo para que sean ejecutadas en distintos CP. Existe un skill lock-in porque el equipo de data saba GCP y el equipo de backend sabe Azure.

## [Service models](https://www.area19delegate.org/on-premises-vs-iaas-vs-paas-vs-saas-a-comparative-study/)
  ![](https://www.area19delegate.org/wp-content/uploads/2018/08/on-premise-iaas-paas.png)

  ## Modelos de responsabilidad compartida
  * [AWS](https://aws.amazon.com/es/compliance/shared-responsibility-model/)
  * [Azure](https://learn.microsoft.com/es-es/azure/security/fundamentals/shared-responsibility)
  * [GCP](https://cloud.google.com/architecture/framework/security/shared-responsibility-shared-fate?hl=es-419)

## [Alta Disponibilidad](https://aws.amazon.com/blogs/mt/establishing-rpo-and-rto-targets-for-cloud-applications/):
Mantener un sistema funcionando incluso cuando ocurren problemas, minimizando el tiempo de inactividad y asegurando servicios continuos

* RTO (Tiempo de Recuperación Objetivo): El tiempo máximo deseado para que un sistema vuelva a funcionar después de una falla, reduciendo el impacto del tiempo de inactividad.

* RPO (Punto de Recuperación Objetivo): La cantidad máxima de datos que una organización está dispuesta a perder en una interrupción, marcando cuán actualizados deben estar los datos recuperados.

## Tolerancia a Fallos: 
La tolerancia a fallos es la capacidad de un sistema, aplicación o servicio para continuar funcionando de manera aceptable incluso cuando uno o varios componentes experimentan problemas o fallas. Implica diseñar sistemas de manera que sean capaces de manejar errores y problemas sin que todo el sistema se vea comprometido, lo que garantiza la disponibilidad y la continuidad de los servicios incluso en condiciones adversas.

### Cloud provider disaster and recovery documentation
* [AWS](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)
* [Azure](https://azure.microsoft.com/en-us/solutions/backup-and-disaster-recovery/)
* [GCP](https://cloud.google.com/architecture/dr-scenarios-planning-guide?hl=es-419)

## [Escalabilidad](https://azure.microsoft.com/es-es/resources/cloud-computing-dictionary/scaling-out-vs-scaling-up/#overview):
Es la capacidad de incrementar o decrementar los recursos necesarios para complir la demanda cambiante en una aplicación o servicio. Crecer y decrecer basado en la demanda que recibe nuestra aplicación. Ejemplo: descuentos por pago en Black Friday. Entonces, los servicios que reciben pago crezcan y soporten al incremento de la cantidad de usuarios por la oferta y luego de pasada la oferta estos mismos servicios decrecen

  * ESCALABILIDAD VERTICAL: es la escalabilidad de añadir más recursos a un nodo particular dentro de un sistema. Hay una caída del servicio mientras se hace el cambio. Ejemplo: A un determinado servidor lo apago, le aumento los recursos (cpu, ram, disco) y lo vuelvo a prender. Luego tendré que apagarlos para volver a los recursos a sus niveles anteriores. No cambia la cantidad de servidores. Hubo caída del servicio cuando lo apago.

  * ESCALABILIDAD HORIZONTAL: es la capacidad de agregar más nodos para soportar una demanda creciente de solicitudes en un sistema. Ejemplo: replicar servidores en el momento de más carga. No tenemos DOWNTIME (caída del servicio).

¿Sirve ESCALABILIDAD sin alta DISPONIBILIDAD? La ESCALABILIDAD está en más de una ZONA. Porque si solo escalamos en una zona perdemos ALTA DISPONIBILIDAD.
