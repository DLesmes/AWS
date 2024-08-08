## Visión general de las TI tradicionales

Entendamos primero como funciona la web en términos simples. Tenemos un cliente con una dirección IP que se conecta a una red para hacer una petición a un servidor con otra dirección IP. Este servidor devuelve una respuesta al cliente.

Si la web fuera un servicio postal, el cliente seríamos nosotros con la petición o paquete que queremos enviar, la red sería el servicio postal en sí y el servidor representaría al destinatario al que queremos enviar el paquete.

#### ¿Cómo está compuesto un servidor?
Un servidor posee los siguientes componentes:

* Cómputo/CPU: Realiza las operaciones que necesitamos.
* Memoria RAM: Contiene la información a procesar mediante la CPU. Es como un cerebro
* Almacenamiento: Archiva datos, a modo de archivos de texto plano.
* Bases de datos: Información almacenada de manera estructurada
* Redes: Cables, routers y servidores conectados unos a otros. Servidores DNS

#### Terminología de IT (redes)

En términos generales, un cliente envía un paquete a un router, el cual reenvía este paquete al switch, y este se encarga de distribuirlo.

* Router: dispositivo que reenvía paquetes de datos entre redes informáticas
* Switch: dispositivo que toma paquetes y los envía al servidor/cliente correcto en la red

#### Diseño tradicional de infraestructura

Las grandes empresas de IT empezaron comprando servidores y montándolos en sus garajes. Se encontraron con problemas al tratar de expandir su infraestructura, como los costos de mover estos servidores, comprar nuevos, y más…

Problemas del enfoque de IT tradicional
A continuación, conocerás algunas dificultades del enfoque de tecnología de la información habitual:

* Renta: los costos de rentar espacios para mantener servidores son altos
* Mantenimiento: el funcionamiento de los servidores es difícil de asegurar
* Remplazar y agregar hardware: pueden existir largos tiempos de espera para conseguir el hardware necesario
* Escalamiento limitado: podemos vernos limitados por el espacio donde almacenamos los servidores
* Monitoreo 24/7: debemos contratar gente para monitorear los servidores
* Desastres naturales: ¿cómo evitamos que se caigan nuestros servicios si ocurre un imprevisto?

## Qué es la computación en la nube
La computación en la nube es la entrega bajo demanda de computación, almacenamiento de bases de datos, aplicaciones y otros recursos de TI a través de una plataforma de servicios en la nube por medio de Internet con precios de pago por uso.

* Suministras el tipo y tamaño exactamente correctos de los recursos informáticos que necesitas.
* Puedes acceder al instante a todos los recursos que necesitas.
* Una forma sencilla de acceder a servidores, almacenamiento, bases de datos y un conjunto de servicios de aplicaciones: poder de computo, almacenamiento y bases de datos.

##### Servicios que ya has usado en la nube
* Gmail Servicio de email en la nube. Pagas solo por tus emails almacenados (no infraestructura)
* Dropbox Servicio de almacenamiento en la nube. Originalmente se construyó en AWS
* Netflix Servicio de video en demanda. Construido en AWS.

### Tipos de modelos de computación en la nube

##### Nube Privada
* Servicios de nube usados por una organización (no está expuesta al público).
* Control total.
* Seguridad para aplicaciones sensibles.
* Satisface necesidades comerciales específicas. 

##### Nube Pública
* Recursos propios en la nube y operados por proveedores de nube de terceros a través de internet.
* Seis ventajas del cómputo en la nube.
* Google Cloud Platform (GCP), Azure, AWS

##### Nube Híbrida
* Mantener algunos servidores en las instalaciones y extender otras capacidades en la nube.
* Control sobre activos sensibles en tu infraestructura privada
* Flexibilidad y rentabilidad de la nube pública.

#### 5 características de la computación en la nube
* Autoservicio en demanda
* Amplio acceso a la red
* Múltiples inquilinos y agrupación de recursos
* Elasticidad y escalabilidad
* Servicio medido

#### 6 ventajas de la computación en la nube
* Gastos de capital comercial (capex) sobre gastos operativos (opex)
* Economías de escala
* Dejar de adivinar la capacidad
* Incrementar la velocidad y la agilidad
* Dejar de gastar dinero en la ejecución
* Globalizar en minutos

#### Problemas resueltos por la nuble
* Flexibilidad: cambia los tipos de recursos cuando sea necesario
* Rentabilidad: pagar sobre la marcha por lo que se usa
* Escalabilidad: acomodar cargas grandes al hacer que el hardware sea más fuerte o agregando nodos adicionales
* Elasticidad: capacidad de escalar cuando sea necesario
* Alta disponibilidad y tolerancia a fallos, crecer en todos los centros de datos
* Agilidad: desarrollar, probar y ejecutar rápidamente aplicaciones en la nube

## Los diferentes tipos de cómputo: IaaS vs. PaaS vs. SaaS

Ahora que conoces más sobre la tecnología en la nube, es importante introducir sus distintos tipos de servicio en la industria para identificar sus diferencias.

Estos modelos varían de acuerdo al tipo de servicio informático que pueda ofrecer, como servidores, almacenamiento, software o bases de datos.

#### Infrastructure as a Service (IAAS)
La infraestructura como servicio (IAAS) proporciona componentes básicos de IT en la nube, es decir, redes, computación, almacenamiento, etc. A su vez, provee el máximo nivel de flexibilidad para adaptarlo a tus necesidades.

* Azure Virtual Machines
* Linode
* Digital ocean
* S2 AWS

#### Platform as a Service (PAAS)
Los modelos que ofrecen una plataforma como servicio (PAAS) eliminan la necesidad de que administremos la infraestructura y proveen una plataforma para gestionar aplicaciones.

* Heroku
* Google App Engine
* AWS Elastic Beanstalk

#### Software as a Service (SAAS)
El Software como servicio (SAAS) brinda un producto de software terminado que es ejecutado y administrado por el proveedor del servicio.

* Amazon Rekognition
* Dropbox
* Zoom
* Gmail

#### On -premises
On-premises se refiere a una forma tradicional de cómputo en la cual nos encargamos de gestionar nuestra propia infraestructura.

### Responsabilidades según el tipo de cómputo

En la siguiente tabla se muestra qué componentes de IT están administrados según el tipo de cómputo en la nube. “Sí” indica que el componente está administrado por el proveedor de nube, “No” indica que nosotros somos responsables del componente.

| Componente | On-premises | IAAS | PAAS | SAAS |
|---|---|---|---|---|
| Aplicaciones | No | No | No | Sí |
| Data | No | No | No | Sí |
| Runtime | No | No | Sí | Sí |
| Middleware | No | No | Sí | Sí |
| O/S | No | No | Sí | Sí |
| Virtualización | No | Sí | Sí | Sí |
| Servidores | No | Sí | Sí | Sí |
| Almacenamiento | No | Sí | Sí | Sí |
| Redes | No | Sí | Sí | Sí | 

