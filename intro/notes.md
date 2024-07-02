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
