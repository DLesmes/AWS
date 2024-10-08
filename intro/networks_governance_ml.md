# Notes Networks, Governance and Machine Learning Fundamentals 😉

## AWS Networking: Connecting Your Cloud World 🌐

Networking is all about how computers and other tech devices communicate with each other.  It&#39;s the foundation of the internet, a vast network of computers accessible to everyone.  The internet relies on IP addresses, routers, DNS, and security to function.  AWS offers powerful networking services that simplify building networks and delivering content to users quickly and efficiently.

**Cloud Networking: Building Your Private Cloud Network**

AWS provides services to set up and manage your own private cloud networks:

* **Amazon Virtual Private Cloud (VPC):** Create your own private network within AWS, isolated from other users, giving you complete control over IP addressing, subnets, and routing.  It&#39;s like having your own slice of the AWS cloud! 🍰☁️
* **AWS Transit Gateway:** Connect multiple VPCs and your on-premises networks through a central hub, simplifying network management and improving security.  Think of it as a central traffic controller for your cloud network. 🚦
* **AWS PrivateLink:**  Establish private connections between VPCs and on-premises applications without exposing your traffic to the public internet, enhancing security and reducing latency.  
* **Amazon Route 53:** Host your own managed DNS service, ensuring reliable and fast domain name resolution for your applications. 

**Networking at Scale: Handling Massive Traffic with Ease 💪**

These services help you scale your network traffic to meet even the most demanding needs:

* **Elastic Load Balancing:** Automatically distribute incoming traffic across multiple resources, such as EC2 instances, to improve scalability, availability, and fault tolerance.  
* **AWS Global Accelerator:**  Route traffic through AWS&#39;s global network infrastructure to enhance performance for global applications.  It&#39;s like giving your applications a super-fast lane on the internet! 🚀
* **Amazon CloudFront:**  A content delivery network (CDN) that securely delivers data, videos, and applications to users worldwide with low latency and high transfer speeds. CloudFront caches content closer to users, ensuring faster load times and a better user experience. 

AWS provides a comprehensive suite of networking services to help you build secure, scalable, and high-performance cloud networks. 

## Amazon VPC: Your Private Network in the Cloud ☁️🔒
![](https://static.platzi.com/media/user_upload/natgateway-4443fbf2-58ac-416b-b9ee-d29c9b7ae0dc.jpg)

Think of a VPC (Virtual Private Cloud) as your own exclusive neighborhood within the vast AWS city.  It's a private network where you control who gets in and out. 🏘️

**Network Interfaces: Your Gateway to Connectivity**

Every computer connected to another needs a network interface. It acts as a bridge between your computer and the technology used for the connection (like cables, routers, or Wi-Fi). 

**IP Addresses: Your Digital Home Address 🏘️**

Once computers are connected, you need a network setup, and that's where IP addresses come in. Think of an IP address as your computer&#39;s unique identifier in the digital world.

**IP Address Ranges:  Your Private Neighborhood**

An IP address range is like a gated community for your devices.  They can only communicate with other devices within the same network.  Each device gets its own IPv4 address, a set of four numbers (0-255) separated by dots. Private networks use specific IP ranges:

* 10.0.0.0 
* 172.16.0.0
* 192.168.0.0

**[Amazon VPC](https://docs.aws.amazon.com/es_es/vpc/latest/userguide/what-is-amazon-vpc.html): Your Cloud Neighborhood Builder 🏗️**

Amazon VPC lets you create a virtual network within AWS, using your own private IP address range (e.g., 10.0.0.0/24, covering IPs from 10.0.0.0 to 10.0.0.255). This VPC becomes a secure zone for your virtual machines and other AWS services. 

**Amazon VPC Components: Controlling the Flow of Traffic 🚦**

Here are some key components of Amazon VPC for managing traffic:

* **[NAT Gateway](https://www.youtube.com/watch?v=FTUV0t6JaDA):**  [Enables your instances to access the internet without having public IP addresses, enhancing security](https://docs.aws.amazon.com/es_es/vpc/latest/userguide/vpc-nat-gateway.html). 🌐➡️💻
* **Internet Gateway:**  Allows traffic from the internet to reach your EC2 instances, making your applications publicly accessible.  🌐➡️💻
* **Network ACLs (Access Control Lists):**  Act as firewalls for your subnets, controlling inbound and outbound traffic based on rules you define.  🚧

Amazon VPC gives you the power to create a secure, isolated, and customizable network environment for your AWS resources. You control the connectivity, security, and access, just like in your own private network. 

## Amazon CloudFront:  A Global Content Delivery Network for Blazing-Fast Websites 🌎⚡️

Before we delve into CloudFront, let's recall how AWS ElastiCache works. ElastiCache caches database requests, speeding up data retrieval by reducing the need to hit the database every time. It sits between your website and your database.

CloudFront operates similarly, but it sits between your users' browsers (or clients) and your website. Its mission is to deliver data, applications, and websites worldwide with incredibly low latency. 

**Edge Locations:  CloudFront's Global Network**

AWS has strategically placed edge locations around the world. These are points of presence from which CloudFront can serve content, ensuring your users get the fastest possible experience. 

**How CloudFront Works: Caching for Speed ⚡**

1. **User Request:** A user tries to access your website.
2. **CloudFront Interception:** CloudFront intercepts the request.
3. **Edge Location Routing:** CloudFront automatically routes the request to the nearest edge location.
4. **Cached Content:**  If the requested content is already cached at the edge location, it's delivered directly to the user, resulting in lightning-fast load times.
5. **Content Updates:** If the cached content has expired, CloudFront checks your origin server (your website's hosting location) for a newer version. If updated, the new version is cached and served. Otherwise, the cached version is delivered.
6. **Global Replication:** Any changes you make to your website's content are replicated across all edge locations as users access it, ensuring everyone gets the latest version quickly.

**Benefits of CloudFront:  Speed, Security, and More 💪**

* **Security:**  CloudFront provides protection against DDoS attacks, acting as a shield for your origin servers. It also gracefully handles traffic spikes, ensuring your website stays up and running. 🛡️
* **Edge Computing:** You can run AWS Lambda functions at edge locations to customize content delivery and add dynamic functionality. 
* **Real-Time Monitoring:** CloudFront provides comprehensive real-time metrics, giving you visibility into your content delivery performance. 📈
* **Cost-Effective:**  CloudFront's pay-as-you-go pricing model makes it an affordable solution for accelerating your website's performance. 💰

CloudFront is a powerful tool for delivering lightning-fast and secure web experiences to users around the globe. It takes care of the complex logistics of content distribution, allowing you to focus on building amazing websites and applications. 
