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
| Aplicaciones | ❌ | ❌ | ❌ | 👍 |
| Data | ❌ | ❌ | ❌ | 👍 |
| Runtime | ❌ | ❌ | 👍 | 👍 |
| Middleware | ❌ | ❌ | 👍 | 👍 |
| O/S | ❌ | ❌ | 👍 | 👍 |
| Virtualización | ❌ | 👍 | 👍 | 👍 |
| Servidores | ❌ | 👍 | 👍 | 👍 |
| Almacenamiento | ❌ | 👍 | 👍 | 👍 |
| Redes | ❌ | 👍 | 👍 | 👍 | 

## Una pequeña historia de AWS

Benjamin Black and Chris Pinkham, the masterminds behind Amazon Web Services, saw a need for groundbreaking tech solutions during a surge in traffic and demand. Their vision laid the foundation for a revolution in cloud computing.

##### A History of Innovation 💡
AWS has become a cornerstone for countless startups and established companies alike, driving transformations across industries.

###### A Timeline of Milestones ⏳
Here's a quick and easy look at the key moments in AWS's history:

* 2002 ➡️ The platform is born within Amazon!
* 2003 ➡️ AWS starts its journey to the world.
* 2004 ➡️ SQS (Simple Queue Service) makes its debut.
* 2006 ➡️ SQS, S3 (Simple Storage Service), and EC2 (Elastic Compute Cloud) launch to the public. 🚀
* 2007 ➡️ AWS expands its reach across Europe. 🌎
* 2009 ➡️ RDS (Relational Database Service) joins the lineup.
* 2010 ➡️ Route 53, a domain name system, becomes available.
* 2012 ➡️ DynamoDB (a non-relational database) revolutionizes data management.

###### AWS: By the Numbers 📊

You might be a devoted AWS user, but did you know these facts? 🤔

* 2019 ➡️ AWS reached a staggering $35.02 Billion in annual revenue! 🤑
* 2019 ➡️ AWS commanded a massive 47% of the cloud market! 📈
* Active Users: AWS has over 1 Million active users! 🤯

AWS has come a long way, and its story continues to inspire! 🚀

## Una visión global: regiones y zonas de disponibilidad

AWS infrastructure is a global network, built with regions, availability zones, data centers, and points of presence. Let's explore its key components:
Regions Around the World 🗺️
AWS boasts a vast global presence, with regions scattered across the globe, like Ohio, Oregon, Northern California, and even government-specific locations like GovCloud East in the US. Want to see the full list? Check out this AWS page! [[Link to AWS page](https://aws.amazon.com/es/about-aws/global-infrastructure/?p=ngi&loc=0)].

##### Choosing the Right Region 🤔
Selecting the right AWS region for your applications depends on a few key factors:
* Compliance: Data residency and governance laws are paramount. AWS ensures your data stays within a region unless you explicitly authorize otherwise. 🔒
* Proximity: Minimize latency and ensure smooth user experiences by launching your application in a region closest to your users. Check out cloudping.info to gauge latency from your location to various regions. ⚡️
* Service Availability: Some services are global (available everywhere), while others are regional (limited to specific locations).

###### Global Services
* IAM (Identity and Access Management): Manage user permissions and security.
* Route 53: A global DNS service.
* CloudFront: A content delivery network (CDN).
* WAF (Web Application Firewall): Protect your web applications. 🛡️

###### Regional Services:
* EC2 (Elastic Compute Cloud): Virtual servers.
* Beanstalk: A platform-as-a-service (PaaS) for web applications.
* Lambda: A serverless compute service.
* Rekognition: An image and video analysis service. 🖼️
* Pricing: AWS pricing is transparent and varies across regions. You can find detailed pricing on the service pages. 💰

#### Availability Zones: A Closer Look 🏘️

Each availability zone is a cluster of data centers, each packed with servers. These data centers are designed with high availability in mind, featuring redundant power, network infrastructure, and connections. They are physically separated for added resilience. 💪

#### Shared Responsibility: Who Does What? 🤝

AWS and its clients have specific responsibilities within the cloud environment.

##### AWS takes care of:
* Hardware & Global Infrastructure: The physical hardware and global network infrastructure.
* Regions: The geographic locations for data centers and services.
* Availability Zones: The clusters of data centers within regions.
* AWS Edge Locations/Points of Presence: Points of presence for content delivery and edge computing.
* Software: Operating systems, virtualization, and other core software components.
* Compute: Providing virtual servers and compute resources.
* Storage: Managing storage services like S3.
* Databases: Providing database services like RDS and DynamoDB.
* Networking: Managing the global network infrastructure.

##### The client is responsible for:
* Operating System Updates: Keeping operating systems secure and up-to-date.
* Data Protection: Securing and managing data stored on AWS. 🔐
* Application Management: Developing, deploying, and managing applications.
* Access Control: Configuring and managing access to AWS resources.
* User and Group Management: Managing users, groups, and permissions within their applications.

This breakdown gives you a better understanding of the components that make up AWS and how it works. Remember, AWS offers a wide range of services and resources to support your cloud computing needs.


## Seguridad e identidad 📡

Moving your applications to the cloud is a big step, and security is paramount. It's crucial to protect your data and ensure users have access only to the resources they need.

### Data Protection Services
AWS offers a variety of services to safeguard your data:
* Amazon Macie: 🕵️‍♀️ This service helps you discover and protect sensitive data by automatically scanning your data stores and identifying potential risks.
* AWS Key Management Service (KMS): 🔐 KMS is your key to encryption! It securely stores and manages your encryption keys, making it easier to encrypt and decrypt data.
* AWS CloudHSM: 🔒 For the highest level of security, CloudHSM provides hardware-based key storage, adding an extra layer of protection.
* AWS Certificate Manager: 🌐 Certificate Manager streamlines the process of obtaining, managing, and deploying SSL/TLS certificates, ensuring secure communication.
* AWS Secrets Manager: 🤫 Secrets Manager securely stores and retrieves sensitive data like passwords, API keys, and database credentials.

### Infrastructure Security Services
Protecting your infrastructure is just as vital as securing your data. AWS provides these services:
* AWS Shield: 🛡️ AWS Shield is your shield against DDoS attacks (Denial of Service). It protects your applications from malicious traffic that could overwhelm your systems.
* AWS Web Application Firewall (WAF): 🚧 WAF acts as a barrier, filtering malicious web traffic to keep your web applications safe.
* AWS Firewall Manager: 👮‍♂️ Firewall Manager centralizes firewall rule management, making it easier to enforce consistent security policies across your AWS resources.

### Threat Detection Services
AWS offers a suite of services for proactive threat detection:
* Amazon GuardDuty: 🚨 GuardDuty automatically detects threats across your AWS environment, constantly monitoring for suspicious activity.
* Amazon Inspector: 🔎 Inspector helps analyze the security posture of your applications, identifying vulnerabilities and configuration issues.
* Amazon Config: 📝 Config continuously tracks and evaluates the configuration of your resources, ensuring they comply with your security policies.
* Amazon CloudTrail: 👣 CloudTrail records user activity and API calls made to your AWS account, providing valuable audit trails for security investigations.

### Identity and Access Management (IAM) Services
AWS offers several services for managing user identities and access control:
* AWS Identity and Access Management (IAM): 🔑 IAM is the cornerstone of access control. It helps you securely manage who has access to your AWS accounts, services, and resources.
* AWS Single Sign-On (SSO): 🚪 SSO streamlines user logins. It enables users to sign in once and access multiple AWS applications and resources.
* Amazon Cognito: 👤 Cognito helps users manage their identities within your applications, providing a seamless user experience.
* AWS Directory Service: 🏢 Directory Service allows you to manage and implement an Active Directory service, making it easier to integrate existing user directories with AWS.
* AWS Organizations: 🏗️ Organizations provides a centralized way to govern and manage multiple AWS accounts, streamlining administration and security policies.

Remember: AWS provides a comprehensive suite of services to protect your data, infrastructure, and user identities. By leveraging these services, you can build a secure cloud foundation for your applications.

##  Secrets Manager: Your Secure Key Vault 🔐 

Secrets Manager is a fantastic AWS service that helps us keep our sensitive data safe and sound!  It protects secrets like passwords, API keys, and tokens, which are vital for accessing our applications, services, and resources. 

Think of it as a secure vault where we can store our most valuable information.  🤫

**Sharing Secrets with Ease 🤝**

Secrets Manager also makes it easy to share these secrets with others when needed, without having to copy and paste them directly into our code.  This helps us avoid security risks and keeps our applications running smoothly. 

**No More Copy-Pasting!  🙅‍♀️** 

By using Secrets Manager, we eliminate the need to hardcode secrets into our applications. This makes our code cleaner, more secure, and easier to manage. 

Secrets Manager helps us focus on building great applications while ensuring our sensitive data stays protected.  💪 

##  Directory Services:  Managing User Access and Security 🔐

A directory acts like a central hub 🏢, storing login information for everyone on a network and enabling security policy enforcement. 

**Microsoft's Active Directory: The Industry Standard 👑**

Because Windows is the world's most popular operating system, Microsoft created Active Directory to help businesses manage user logins for their employees. 

**AWS Directory Service:  Your Cloud-Based Solution ☁️**

AWS Directory Service is a managed service that brings the power of Active Directory to your AWS resources!  

**Key Benefits of AWS Directory Service:**

* **No Server Hassle:**  AWS Directory Service takes care of managing your Active Directory, so you don't need to set up and maintain servers manually.  🙌
* **Simplified Directory:**  Choose from a variety of Active Directory options, including a simplified version that's perfect for smaller businesses. 
* **AWS Integration:** The AWS Directory Connector allows users to access AWS applications using their existing Active Directory credentials.  🔐 
* **High Availability:**  AWS Directory Service is built for reliability, with automatic error recovery in case of server failures. 
* **AWS Ecosystem Integration:**  AWS Directory Service seamlessly integrates with other AWS services, making it a valuable addition to your cloud environment.

**Want to learn more?**  Explore the AWS Directory Service documentation!  [[Link to AWS Documentation](https://aws.amazon.com/es/directoryservice/)]  

## 6 Reasons to Embrace Cloud Computing with AWS  ☁️

AWS brings a world of benefits to your business!  Here are 6 key advantages:

1. **Say Goodbye to Capital Expenses!** 👋  AWS operates on a pay-as-you-go model, so you only pay for the resources you use.  No more upfront investments in hardware! You can also reduce your overall ownership and operational costs. 
2. **Scale with Ease and Savings!** 📈  AWS leverages economies of scale. As your demand grows, your costs decrease!
3. **Predictable Scaling and Cost Control:**  No more guessing how much capacity you need! AWS lets you scale your applications based on real-time usage. This helps you optimize your resource allocation and control costs effectively. 
4. **Speed and Agility at Your Fingertips:** ⚡️  With AWS, you can deploy applications and services faster than ever before.  Enjoy the freedom to adapt and innovate quickly!
5. **Free Up Time and Resources:**  Say goodbye to the hassle of managing your own data center!  AWS takes care of the heavy lifting, freeing up your time and resources to focus on what truly matters. 
6. **Go Global in a Flash:**  🌎  AWS lets you expand your platform to a global audience with just a few clicks.  Reach customers worldwide instantly! 

AWS offers a powerful and flexible solution that can help your business grow and thrive.  🚀 
