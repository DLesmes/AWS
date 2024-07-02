# Notas de clase

## Razones para usar la nube
  
  * Las Pymes mejoran su economía y costos después de adoptar la nube.
  * Es una de las diez habilidades mejor pagadas en la actualidad. ' 
  * Almacenanmiento y acceso a la información:++ Cloud almacena grandes cantidades de información hasta hexabytes, puedes acceder a ella en cualquier lugar del mundo y brinda seguridad de calidad para la misma.
  * Escalable y flexible:++ Las aplicaciones pueden escalar de pocos a muchos más usuarios de forma flexible y soporta las altas demandas y, el cloud permitirá crecer basado en las necesidades de las empresas
  * ++Agiliad:++ En poco tiempo puedes crear una aplicación y automatizar el despliegue y servicios lo que te permite enfocarte en la aplicación y su desarrollo.
  * ++Reducción de costos:++ Una de las grandes ventajas del Cloud es que los costos se generan de acuerdo a las necesidades ''Pago por demanda''
  * ++Innovación e Inteligencia Artificial:++. Puedes acceder a servicios de realidad aumentada o detección de fraudes. Los proveedores de Cloud ya ofrecen servicios para aplicar la IA, Machine Learning o DataScience.

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
