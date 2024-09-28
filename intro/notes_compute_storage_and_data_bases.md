## AWS Compute

AWS describes its compute capabilities as "compute for any workload". Compute refers to using a computer for processing, whether it's adding two numbers or hosting a website. Let's explore the compute services AWS has to offer:
### Instances or Virtual Machines 🖥️
A virtual machine (VM) is software that simulates an operating system, allowing you to run programs as if you had a real physical computer. Here are the VM services in AWS:
* Amazon EC2: Secure and resizable virtual machines. 🏗️
* Amazon EC2 Spot: Cost-effective for fault-tolerant workloads, up to 90% cheaper than normal instances. But be warned - Amazon can reclaim these at any time with just two minutes' notice! ⚠️
* Amazon EC2 Auto Scaling: Automatically scales your compute capacity up or down based on demand, ensuring you have the resources you need when you need them. 📈📉
* Amazon EC2 LightSail: A user-friendly platform to launch applications or websites quickly and easily. 🚀
#### Containers 📦
A container is a unit of software that packages an application and its dependencies. Unlike VMs that virtualize hardware, containers virtualize the operating system. AWS container services include:
* Amazon Elastic Container Service (ECS): Run reliable and scalable containers. 🚢
* Amazon Elastic Container Registry (ECR): Store, manage, and deploy container images. 🐳
* Amazon Elastic Kubernetes Service (EKS): A managed Kubernetes service by AWS. ☸️
#### Serverless ⚡
Serverless computing takes the hassle out of managing servers or VMs. It lets you focus on your application code. Amazon Lambda lets you run code without provisioning or managing servers.
#### Edge Services 🌎
Edge computing brings computation and data processing closer to where it's needed. AWS edge computing services include:
* Amazon Outposts: Run AWS services on your own premises instead of in Amazon's data centers. 🏢
* Amazon Snow Family: A family of devices ranging from portable hard drives to entire semi-trailers filled with storage. Load your data onto these devices and ship them to Amazon for secure upload. 🚚
* AWS Wavelength: Access AWS services from 5G devices without going over the public internet. 📶
* VMware Cloud on AWS: Migrate your VMware workloads to AWS seamlessly. 🔄
* AWS Local Zones: Run your applications closer to end users for lower latency. 🏎️

## EC2: Your Virtual Machine Powerhouse ⚡️🚀
**Elastic Compute Cloud** lets you rent virtual machines, known as EC2 instances. You can choose from different types of EC2 instances, each with varying CPU power, RAM, and storage options. There are instances optimized for compute, memory, storage, and other specialized workloads.
#### Pay-As-You-Go Flexibility 💰
EC2's most common payment system is hourly or per-second billing, depending on the instance type. For example, an instance costing $0.10 per hour allows you to run one instance for 24 hours or 24 instances for one hour, both costing the same ($2.40).
#### On-Demand Options and Pricing 💸
Instances can be easily resized. Start with a low-cost instance and if you need more power, simply stop the instance, choose a new instance type, and restart. Voila! Your instance now has more capacity. 🪄
Here are some examples of EC2 instance types:
| Name         | Specifications                | Price           |
|--------------|-------------------------------|-----------------|
| t3.nano      | 2 vCPUs, 0.5 GiB RAM       | $0.0052/hour     |
| t3.xlarge    | 4 vCPUs, 16 GiB RAM        | $0.1664/hour    |
| c6g.8xlarge  | 32 vCPUs, 64 GiB RAM       | $1.088/hour     |
| X1e.xlarge   | 128 vCPUs, 3904 GiB RAM, 2x 1920 GB SSD | $26.688/hour   |
#### Dedicated Hosts: Your Private Cloud Enclave 🔒
Dedicated Hosts in AWS are like your own private server haven within the AWS cloud. Instead of sharing physical servers with other users, you get exclusive access and control over your EC2 instances' placement and allocation. This is perfect for applications needing:
* **Enhanced Security:** Keep your data extra safe. 🔐
* **Regulatory Compliance:**  Meet strict industry standards. ✅
* **Consistent Performance:**  Experience predictable and reliable performance. 📈

Dedicated Hosts also let you bring your existing software licenses to the cloud without added costs. 💰
Even AWS beginners can benefit from Dedicated Hosts, enjoying greater resource isolation and predictability while leveraging the scalability and flexibility of AWS. ☁️

## Docker and Amazon ECS: Containerization Made Easy 📦 🚀

Imagine packaging your application, its libraries, and dependencies, all with their specific versions, into a neat little box. This box, called a container, can be run on any machine without compatibility nightmares.  That's the magic of containerization! ✨

**Solving the Version Headache 🤕**

Software development often involves juggling different versions of libraries, programming languages, and programs. Docker comes to the rescue by letting us create containers that solve this problem. 

**Amazon Elastic Container Service (ECS): Your Container Orchestrator 🚢**

Amazon ECS is a container orchestration service where you can deploy your container images on AWS. It creates a seamless experience, making your local machine and the AWS environment feel like one. 

**Why Containers Rock? 😎**

* **Portability:** 💻➡️☁️ Containers run consistently across different environments, simplifying deployment and migration. 
* **Isolation:**  Each container enjoys its own private space, enhancing security and preventing application conflicts. 🔐
* **Resource Efficiency:**  Sharing resources with the host operating system makes containers leaner and more efficient than virtual machines. 💪
* **Agile Development:**  Containers foster continuous integration and delivery (CI/CD) by providing consistent, reproducible development environments. 🔁

Containers are transforming the way we build and deploy software, and AWS ECS makes it easy to harness their power in the cloud. 

## AWS Lambda:  Embrace the Serverless Revolution! ⚡🐑

AWS Lambda is a game-changer in the world of cloud computing. It&#39;s a serverless service that lets you run code in response to events without the hassle of managing servers or infrastructure.  Events can be anything from timers and application visits to HTTP requests and more.  

Think of it as magic! ✨ You write your code, upload it, and Lambda handles the rest, automatically scaling to meet demand. 

**Lambda in Action: Real-World Use Cases 🧰**

Lambda excels in various scenarios, including:

* **Data Processing at Scale:**  Process vast amounts of data efficiently and cost-effectively. 📈
* **Interactive Backends:**  Power dynamic web, mobile, and IoT applications with serverless backends. 📱💻
* **Seamless Integrations:**  Combine Lambda with other AWS services like S3, DynamoDB, and API Gateway to build robust, scalable applications.  

**Lambda Pricing: Pay Only for What You Use 💰**

Lambda billing is based on milliseconds of execution time and RAM usage.  For instance, running a function with 128MB of RAM for 30 million events per month would cost approximately $11.63. 

**Key Features of AWS Lambda: A Serverless Powerhouse 💪**

* **Serverless Freedom:** No need to worry about servers! AWS handles all the underlying infrastructure, so you can focus on coding. 🤯
* **Auto-Scaling Magic:** Lambda scales automatically based on workload, allocating resources as needed to handle incoming requests. 📈📉
* **Pay-Per-Use Efficiency:** Pay only for the execution time of your code. No fixed fees or idle time charges, making it ideal for variable workloads.  💰
* **AWS Integration Power:**  Lambda seamlessly integrates with other AWS services, allowing you to build complex and interconnected applications. 
* **Event-Driven Architecture:** Lambda runs in response to events, such as database changes, file uploads, messages in queues, and HTTP requests, enabling a flexible and responsive architecture. 👂
* **Multilingual Support:**  Write your Lambda functions in popular programming languages, including Node.js, Python, Java, Go, Ruby, and .NET Core. 💻

Lambda empowers you to build and run applications without server management headaches, scaling effortlessly and offering cost-effective solutions for a wide range of use cases. 

## AWS Storage: Your Data's Cloud Haven ☁️🗄️

Storing data in the cloud means uploading it to a network of servers, where you have access to handy tools for managing and accessing your files from anywhere. 

**Types of Storage and AWS Services**

AWS offers a variety of storage services tailored to different needs.  Let's break down the types of storage:

* **File-Based Storage:** 📁 This familiar approach organizes files in folders and subfolders, just like your computer's file system.  AWS services in this category include:
    * **Amazon Elastic File System (EFS):**  A scalable file system for your applications.
    * **Amazon FSx for Windows File Server:**  A fully managed Windows file server in the cloud.
* **Block Storage:**  🧱  Files are stored in volumes as raw, equally sized chunks of data. This type is often used as hard drives for servers or virtual machines.  
    * **Amazon Elastic Block Store (EBS):**  Provides persistent block storage volumes for EC2 instances. 
* **Object Storage:** 📦  Information is stored as objects, each with a unique identifier. Objects are stored in a flat address space, making it ideal for large-scale data storage.
    * **Amazon Simple Storage Service (S3):**  A highly scalable and durable object storage service. 

**Data Backup: Protecting Your Precious Data 🛡️**

* **Amazon Backup:**  Centrally manage and automate backups across your AWS services, keeping your data safe and sound. 

**Data Transfer: Moving Data with Ease 🚚**

Need to transfer data to or from AWS? AWS offers these services to streamline the process:

* **AWS Storage Gateway:**  A hybrid cloud storage service that provides on-premises access to cloud storage. 🌉
* **AWS DataSync:**  Accelerate data movement to and from AWS, up to 10 times faster than traditional methods. 🚀
* **AWS Transfer Family:**  Securely scale your recurring file transfers to and from Amazon S3 and Amazon EFS using FTP, SFTP, and FTPS protocols.  

**Conclusion 🎉**

We&#39;ve taken a quick tour of AWS storage services and the different storage types available.  AWS provides a comprehensive set of tools to help you store, manage, and protect your data in the cloud. 

## Amazon S3: Your Object Storage Powerhouse 🧰 📦

Amazon S3 is a leading object storage service that boasts an impressive 99.999999999% (11 nines!) durability guarantee.  Your data is in safe hands! 🛡️

**S3 Storage Classes: Choose the Right Fit for Your Data**

Amazon offers various S3 storage classes to meet your specific data access and availability requirements.

* **S3 Standard:**  🥇 The gold standard for frequently accessed data, offering high durability, availability, and performance. 
* **S3 Standard-IA (Infrequent Access):**  🥈 For less frequently accessed data that still needs quick retrieval when required. Saves you money compared to S3 Standard.
* **S3 One Zone-IA:** 🥉  Similar to Standard-IA, but even more cost-effective because it stores data in only one Availability Zone (AZ), unlike other S3 classes which use at least three. 
* **S3 Glacier:** 🧊  The go-to choice for long-term archival storage of data you rarely access.  It offers the lowest storage cost, starting at just $1 per TB per month! Glacier provides options for expedited, standard, or bulk data retrieval. 
* **S3 Glacier Deep Archive:** ❄️ The most economical storage class in Amazon S3, perfect for long-term retention and digital preservation of data accessed once or twice a year. 
* **S3 Intelligent-Tiering:** 🧠 This smart storage class automatically moves data between different S3 storage tiers based on usage patterns, helping you optimize costs. 

**Conclusion: The Right Storage for the Right Job ✅**

With Amazon S3, you have a range of options to suit your needs.  Need high availability and durability? S3 Standard is your champion. Looking for long-term, cost-effective archival storage? S3 Glacier is your best bet.  Choose the best fit for your specific use case, and enjoy the power and flexibility of S3! 

## [Amazon EFS](https://aws.amazon.com/es/efs/): Your Elastic File System in the Cloud ☁️📁

Amazon Elastic File System (EFS) is a game-changer for managing shared file storage in the cloud.  It's like having a super-powered network drive for your EC2 instances, but with extra perks! ✨

**NFS: Your File Sharing Superhero 🦸‍♂️**

EFS uses the Network File System (NFS) protocol, allowing your EC2 instances to access files and directories as if they were stored locally, even though they're in the cloud. This means thousands of machines can connect to EFS and work together seamlessly on shared data. 

**EFS Features: Resilient, Secure, and Flexible 💪🔒**

EFS is built for resilience and high availability:

* **Multi-AZ Durability:**  Your files are replicated across multiple Availability Zones within a region, protecting them from outages. 🛡️ 
* **Storage Classes:** Choose between Standard and Standard-IA storage classes.  Set policies to automatically transition files to Standard-IA for cost savings on less frequently accessed data. 💰
* **Automatic Encryption:** Your data is encrypted by default, keeping it safe and secure. 🔐

EFS is a powerful and flexible solution for sharing files across your EC2 instances, offering high availability, durability, and built-in security features. 

## [AWS Storage Gateway](https://aws.amazon.com/es/storagegateway/file/): Your Bridge to the Cloud 🌉☁️

AWS Storage Gateway extends the reach of your on-premises infrastructure, giving you access to virtually unlimited cloud storage.  It's like having a magic portal that connects your local systems to the vastness of AWS. ✨

**Three Gateways, Three Ways to Connect 🚪**

Storage Gateway comprises three distinct gateways, each designed for a specific use case:

**1. File Gateway: Your S3 File System 📁**

File Gateway provides SMB and NFS interfaces to Amazon S3, making it seamlessly integrate with both Windows and Linux environments. It's like having a network drive that's actually backed by S3!

* **Seamless File Access:** Your operating system sees a regular file system, while File Gateway transparently handles the storage of files in S3. 
* **AWS Integration:** Once your files are in S3, you can leverage other AWS services for processing, analysis, and more. 

**2. Tape Gateway: Farewell to Physical Tapes 👋📼**

Imagine migrating your physical tape backups to a virtual tape library in the cloud. That's precisely what Tape Gateway does!  

* **Virtual Tape Library:**  Tape Gateway integrates with leading backup software, creating a virtual tape library in AWS.
* **Cost Savings:** Store your virtual tapes in S3 and leverage cost-effective storage classes like S3 Glacier and Glacier Deep Archive for long-term retention. Say goodbye to expensive physical tape management! 
 
**3. Volume Gateway: Block Storage in the Cloud 🧱**

Volume Gateway provides cloud-backed block storage using the iSCSI protocol, making it ideal for applications needing block-level access to data. 

* **Cached Mode:** Primary data resides in S3, while frequently accessed data is cached locally for faster access. 
* **Stored Mode:** All data is stored locally, with asynchronous backups to S3 for added protection. 

**Conclusion: A Gateway for Every Need ✅**

Whether you need to seamlessly integrate your file system with S3, modernize your tape backups, or leverage cloud-backed block storage, AWS Storage Gateway has a solution for you. Choose the right gateway for your needs and enjoy a smooth transition to the cloud! 🚀

## [Dive into AWS Databases](https://aws.amazon.com/es/rds/?p=ft&amp;c=db&amp;z=3): A World of Data at Your Fingertips 🌎🗄️

Databases are structured collections of data, electronically stored and accessed using computer systems. AWS offers a wide array of secure and highly available database engines to suit your specific needs. Let's explore some of the key types:

**Relational Databases:  Structured Data Powerhouses 📊**

Relational databases excel at managing structured data with relationships between tables.  AWS offers these relational database services:

* **Amazon Aurora:** 💫  A cloud-native relational database compatible with both MySQL and PostgreSQL, offering high performance and scalability.
* **Amazon Relational Database Service (RDS):**  ⚙️  A managed relational database service for popular engines like MySQL, PostgreSQL, MariaDB, Oracle BYOL, and SQL Server. RDS simplifies setup, operation, and scaling for your databases. 
* **Amazon Redshift:** 🚀 Designed for analytics, Redshift utilizes SQL to analyze structured and semi-structured data in data warehouses, operational databases, and data lakes. It leverages AWS-designed hardware and machine learning to deliver high performance at any scale, and at an affordable price. Want to learn more? Platzi offers a Redshift course! 

**Key-Value Databases:  Lightning-Fast Data Retrieval ⚡️**

* **Amazon DynamoDB:**  A key-value and document database that provides single-digit millisecond performance at any scale. It's perfect for high-traffic web applications, e-commerce systems, and gaming applications. 

**In-Memory Databases:  Speed Up Your Applications 🏎️**

* **Amazon ElastiCache:**  A fully managed, in-memory caching service that supports real-time and flexible use cases. ElastiCache boosts application performance by caching frequently accessed data. Common uses include session management, gaming leaderboards, and geospatial applications.  ElastiCache supports both Memcached and Redis engines. 

**Document Databases:  Flexible and Scalable for Modern Applications 🍃**

* **Amazon DocumentDB:**  A highly available, durable, fast, scalable, and fully managed database service for running mission-critical MongoDB workloads.  It's ideal for content management, catalogs, user profiles, and more. 

**Conclusion:  The Right Database for the Right Job  ✅**

AWS offers a diverse range of database services to fit your specific data needs and application requirements. We've just scratched the surface here. Stay tuned for deeper dives into each of these services in future lessons! 

## Amazon RDS:  Your Relational Database in the Cloud, Simplified ☁️📊

Amazon RDS makes it a breeze to create, operate, and scale relational databases in the cloud.  Relational databases are all about structured data with relationships between tables. You can query this data using a powerful language called SQL.

**Six Engines to Choose From: Pick Your Perfect Match**

With Amazon RDS, you have the flexibility to choose from six popular relational database engines:

* **MySQL:** The world&#39;s most popular open-source relational database. 🐬
* **MariaDB:** A community-developed fork of MySQL, known for its performance and features. 🐘
* **PostgreSQL:** A powerful, open-source object-relational database system renowned for its reliability and data integrity. 🐘
* **Oracle:**  A widely used enterprise-grade database system known for its robust features and scalability. 🐳
* **SQL Server:**  Microsoft's flagship relational database management system. 🪟
* **Amazon Aurora:**  Amazon&#39;s own cloud-native relational database compatible with MySQL and PostgreSQL, offering high performance and scalability. 💫

**Amazon RDS Advantages:  Ease, Scalability, and Reliability 💪**

Amazon RDS simplifies database management, offering several key advantages:

* **Fully Managed (PaaS):**  Say goodbye to server headaches! RDS handles all the heavy lifting, including setup, patching, and backups. 🧰
* **Highly Scalable:**  Scale your database capacity up or down effortlessly to meet changing demands. 📈📉
* **Multi-AZ Deployment:**  Deploy your database across multiple Availability Zones for high availability and fault tolerance. 🛡️
* **Read Replicas:**  Create read-only replicas of your database to improve performance for read-heavy workloads. 📖
* **Automatic Backups:**  RDS automatically backs up your data, ensuring its safety and recoverability.  💾
* **Pay-As-You-Go Pricing:**  Pay only for what you use, making RDS a cost-effective solution for your database needs.  💰

Amazon RDS takes the complexity out of managing relational databases, providing a scalable, reliable, and cost-efficient solution in the cloud. 

## DynamoDB: Your Key-Value Dynamo for High-Performance Applications ⚡️🔑

DynamoDB is a NoSQL, key-value document database that delivers blazing-fast, single-digit millisecond performance. It&#39;s the perfect choice for applications demanding real-time data updates and low latency. Think of it as a supercharged data store for your high-performance apps! 🚀

**Key-Value Simplicity, Document Flexibility 🧰**

Key-value databases store data as pairs of keys and values or attributes.  DynamoDB takes this a step further by allowing you to store documents, where each key can have a varying number of attributes with different data types. This flexibility makes DynamoDB suitable for a wide range of use cases.

**DynamoDB Features:  Performance, Scalability, and Peace of Mind 💪**

DynamoDB offers a compelling set of features:

* **Fully Managed (PaaS):**  No need to worry about server management. AWS handles all the operational aspects of your database. 🧰
* **Global Reach:**  Operate your database across multiple regions for global reach and low latency. 🌎
* **High Throughput:** DynamoDB can handle massive workloads, processing up to 20 million requests per second. 🤯
* **Built-In Security:** Protect your data with integrated security features like encryption and access control. 🔐
* **Backup and Restore:**  Keep your data safe with automated backups and point-in-time recovery. 💾

DynamoDB is a powerful, scalable, and highly available database service that&#39;s ideal for applications requiring low latency and high throughput. 

## [Amazon ElastiCache](https://aws.amazon.com/es/caching/?nc1=h_ls): Turbocharge Your Applications with In-Memory Caching 🚀⚡️

Imagine a super-fast data store that keeps your frequently accessed information readily available in memory. That&#39;s the magic of Amazon ElastiCache, a fully managed in-memory caching service that unlocks lightning-fast performance for your applications! ⚡

**In-Memory Speed: Serving Data at the Speed of Light 🏎️**

ElastiCache is an in-memory database that stores previously accessed data in a cache, making retrieval incredibly fast.  It's like having a shortcut to your most important data! Accessing cached data is always quicker than querying your primary database. 

**Real-World Example: A News Site's Secret Weapon 📰**

Think of a popular news website with thousands of visitors every day. By storing frequently accessed articles in an in-memory cache like ElastiCache, the site can serve content to readers with blazing speed.  

**ElastiCache Engines: Redis and Memcached - Dynamic Duo 💪**

ElastiCache offers two powerful engines to choose from:

* **Redis:**  A versatile in-memory data store offering advanced features like data structures, pub/sub messaging, and Lua scripting. 🧰
* **Memcached:**  A high-performance distributed memory caching system, ideal for simple key-value caching. 

Both Redis and Memcached are continuously monitored and can be scaled up or down based on your application's needs.  

**ElastiCache Benefits: Speed, Scalability, and Simplicity ✨**

* **Enhanced Performance:** Dramatically improve application response times by serving frequently accessed data from memory. 
* **Scalability on Demand:**  Effortlessly scale your caching capacity up or down to handle fluctuating workloads. 
* **Fully Managed Service:**  AWS takes care of the management and maintenance, so you can focus on building your applications. 

ElastiCache is a powerful tool for boosting application performance, especially for scenarios with high read traffic or frequently accessed data.


