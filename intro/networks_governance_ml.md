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

## [Amazon CloudFront](https://docs.aws.amazon.com/es_es/AmazonCloudFront/latest/DeveloperGuide/Introduction.html):  A Global Content Delivery Network for Blazing-Fast Websites 🌎⚡️

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

## [Amazon Route 53](https://aws.amazon.com/es/route53/): Your DNS Traffic Controller 🚦🌐

DNS (Domain Name System) is like the internet's phone book, translating domain names (e.g., google.com) into IP addresses that computers understand. Route 53 is AWS's highly reliable and scalable DNS service, costing just $0.50 per hosted zone per month.  It comes with a variety of routing policies to direct your traffic effectively.

**Routing Policies:  Guiding Your Traffic Flow**

Route 53 offers several routing policies to customize how user traffic is directed:

* **Simple Routing:** This standard DNS routing directs traffic for a domain to a specific resource, like a web server. 
* **Weighted Routing:**  Distribute traffic across multiple resources associated with a single domain name. You can assign weights (0 to 255) to each resource to control traffic flow.  This is great for testing new website versions with a smaller audience or gradually migrating users to a new site. 
* **Geolocation Routing:**  Serve different resources based on your users' geographic locations. This enables you to tailor content by region or restrict access to certain areas. 🌎
* **Latency Routing:**  Automatically route traffic to the AWS region closest to the user, reducing latency and improving response times. ⚡️
* **Failover Routing:**  Redirect traffic to a healthy resource and automatically switch to a different resource if the primary one becomes unavailable, ensuring high availability. 
* **Multivalue Answer Routing:** Return multiple values (e.g., IP addresses of web servers) in response to DNS queries.  Route 53 checks the health of each resource and only returns values for healthy ones. This can be used to enhance availability and load balancing, but it's not a replacement for a dedicated load balancer.

**Route 53: A Powerful DNS Solution 💪**

Route 53 is a powerful yet affordable DNS service that can help you:

* **Keep your websites fast and highly available.** 🚀
* **Ensure security and scalability.** 🛡️
* **Manage traffic flow with flexible routing policies.** 🚦

It&#39;s a complex but highly valuable tool for managing your domain names and ensuring a smooth user experience. 

## VPC Diagram 🎲🪀
![](https://static.platzi.com/media/user_upload/AWS7-5047ce6b-0603-478d-9aa8-0ea37debb655.jpg)
1. **User Access:**  A user from the internet attempts to access resources within your VPC. 🌐
2. **Internet Gateway:** The user's request first encounters the Internet Gateway, which acts as the entry point to your VPC. 🚪
3. **Router:**  The Internet Gateway directs the traffic to a router within your VPC. 
4. **Subnets:** The router then forwards the traffic to one of two subnets within your VPC. Subnets are logical subdivisions within your VPC, allowing you to segment your network. 
5. **Network ACL (Access Control List):**  Each subnet has a Network ACL that acts as a firewall. The Network ACL examines the incoming traffic and checks if it's allowed based on rules you've configured. 🚧
6. **Access Granted or Denied:** If the Network ACL rules permit the traffic, the user is granted access to the resources within the subnet. If the rules deny access, the user's request is blocked. 🚫

**Key Concepts:**

* **Internet Gateway:** The entry and exit point for traffic between your VPC and the internet.
* **Router:**  A networking device that directs traffic within your VPC.
* **Subnets:**  Logical subdivisions of your VPC, allowing you to segment your network resources.
* **Network ACL:**  A firewall that controls inbound and outbound traffic for a subnet.

**The Big Picture: A Secure VPC Setup 🔒**

The diagram illustrates a common pattern for setting up a secure VPC:

* Subnets are used to separate resources with different security requirements. 
* Network ACLs act as the first line of defense, controlling traffic at the subnet level.
* The Internet Gateway provides controlled access between the internet and your VPC.

By understanding the flow of traffic and the role of each component, you can design and manage a secure and efficient VPC environment for your AWS resources. 


## Building Your VPC: A Step-by-Step Guide 🏗️ 

Here's a breakdown of the instructions for creating a VPC and an Internet Gateway in AWS, enhanced with emojis for better clarity:

**Creating Your VPC:  Your Private Cloud Neighborhood**

1. **Find VPC:** In the AWS search bar, type "VPC" and select the first result.  🔍
2. **Your VPCs:**  Go to "Your VPCs" and click "Create VPC." 
3. **Configuration:**
    * **Name Tag (optional):**  DemoVPCLaboratorio 🏷️
    * **IPv4 CIDR block:** Choose "Manually enter IPv4 CIDR." 
    * **IPv4 CIDR:**  Enter `10.0.0.0/16`. This defines your VPC's private IP address range.
4. **Create:** Click "Create VPC."

![](https://static.platzi.com/media/articlases/Images/2022-05-30%20%281%29.png)

**Creating Your Internet Gateway:  Connecting to the World**

1. **Internet Gateways:** Go to "Internet Gateways" and click "Create internet gateway." 🌐
2. **Name Tag:** Enter "DemoIGWLaboratorio." 🏷️
3. **Create:**  Click "Create internet gateway."
4. **Detached State:**  Your new Internet Gateway will appear with a "Detached" status, as it's not yet connected to a VPC. 
5. **Connect to VPC:** Click "Actions"  ➡️ "Attach to VPC."
6. **Select VPC:** Choose your VPC ("DemoVPCLaboratorio") and click "Attach internet gateway."  Make sure your Internet Gateway and VPC are in the same AWS region! 
7. **Success!** You've now created two key components of your VPC. 🎉

**Key Takeaways**

* A VPC provides a private network for your AWS resources. 🔒
* An Internet Gateway connects your VPC to the internet. 🌐
* Make sure your Internet Gateway and VPC are in the same region. 🌎

These steps guide you through the initial setup of a VPC and an Internet Gateway.  Remember, this is just the foundation of your VPC environment. You'll need to configure other components, such as subnets and routing tables, to build a complete and functional network. 


##  Completing Your VPC Setup: Routing, Subnets, and Security  🏗️

Now that you&#39;ve created your VPC and Internet Gateway, let&#39;s configure the remaining components: routing table, Network Access Control Lists (ACLs), and subnets.

**Creating a Routing Table: Guiding Traffic Flow**

1. **Routing Tables:**  From the VPC service page, go to "Route Tables." 
2. **Default Route Table:** You&#39;ll see a default route table that was automatically created with your VPC. 
3. **Edit Routes:** Select the default route table, go to "Routes," and click "Edit routes."

![](https://static.platzi.com/media/articlases/Images/2022-05-31.png)
5. **Add Route:**  Click "Add route", enter `0.0.0.0/0` in the "Destination" field, select "Internet Gateway" for "Target," and choose the Internet Gateway you created earlier.
6. **Save Changes:** Click "Save changes." This allows all traffic from your VPC to reach the internet via the Internet Gateway.  🌐

![](https://static.platzi.com/media/articlases/Images/2022-05-31%20%281%29.png)
**Creating Network ACLs:  Your VPC Firewall**

1. **Network ACLs:** Go to "Security" in the VPC service page and then to "Network ACLs." 
2. **Create Network ACLs:** Click "Create network ACL."  You&#39;ll create two Network ACLs, one for each subnet. Name them "NACLA" and "NACLB", and select your VPC. 
3. **Create:** Click "Create network ACL." 

![](https://static.platzi.com/media/articlases/Images/2022-05-31%20%282%29.png)
**Adding Inbound and Outbound Rules: Allowing HTTP Traffic**

For each Network ACL, you need to add inbound and outbound rules to allow HTTP traffic on port 80:

1. **Select Network ACL:** Choose "NACLA" or "NACLB." 
2. **Inbound Rules:**  Go to "Inbound rules" ➡️ "Edit inbound rules."

![](https://static.platzi.com/media/articlases/Images/2022-05-31%20%283%29.png)
3. **Add Rule:** Click "Add new rule" and enter these settings:
    * **Rule number:**  100 (rules are evaluated in ascending order) 
    * **Type:**  HTTP (80) 
    * **Source:**  0.0.0.0/0 (allows traffic from anywhere) 
    * **Allow/Deny:** Allow 
4. **Save:** Click "Save changes." 
5. **Repeat:** Repeat the process for outbound rules and for the other Network ACL (NACLB) using the same settings.

![](https://static.platzi.com/media/articlases/Images/2022-05-31%20%285%29.png)
**Creating Subnets: Dividing Your VPC**

1. **Subnets:** Go to "Subnets" and click "Create subnet." 
2. **Choose VPC:** Select your VPC ("DemoVPCLaboratorio") and enter these settings for the first subnet:
    * **Subnet name:** DemoSubredA 
    * **Availability Zone:**  Choose the first availability zone that ends in "a".
    * **IPv4 CIDR block:**  `10.0.0.0/25` (assuming your VPC has a CIDR block of `10.0.0.0/24`)
3. **Create:** Click "Create subnet."
4. **Repeat:** Create the second subnet with these settings:
    * **Subnet name:** DemoSubredB 
    * **Availability Zone:** Choose the second availability zone that ends in "b".
    * **IPv4 CIDR block:**  `10.0.0.128/25` 

![](https://static.platzi.com/media/articlases/Images/2022-05-31%20%286%29.png)

**Associating Network ACLs with Subnets**

1. **Right-click:** Right-click on "DemoSubredA" and select "Edit network ACL association." 
2. **Select ACL:**  Choose the corresponding Network ACL (NACLA). 
3. **Save:**  Click "Save" and repeat the process for "DemoSubredB" and its associated ACL (NACLB). 

**You're Done! 🎉**

You've now created all the essential components of your VPC: Internet Gateway, routing table, Network ACLs, and subnets. You've also granted public access to your subnets via HTTP on port 80. Now you have a secure, customizable, and functional network environment within AWS! 

## [Management and governance with AWS](https://luxurious-expert-b2e.notion.site/Introducci-n-8a641a06afd942c2843f30ed97212abd): Simplified and Optimized 🧰 ☁️

In the past, companies and organizations had to walk a tightrope between innovation and the control of costs, security, and compliance.  AWS management and governance services are here to simplify that balancing act! ✨ These services aim to make managing your AWS environment as easy and optimized as possible.

### Account Management 🔐

These services help you manage your precious AWS accounts:

* **AWS Control Tower:** Easily set up and govern a secure, multi-account AWS environment. Think of it as your command center for cloud governance. 🏗️
* **AWS Organizations:**  Centrally manage and govern your AWS environments across multiple accounts.  Keep things organized and under control. 🗂️
* **AWS Budgets:** Plan and track your AWS costs, ensuring you stay within budget and optimize spending. 💰

### Provisioning Services:  Building Your Cloud Kingdom  🏗️

These services streamline the provisioning, creation, and configuration of new AWS resources:

* **AWS CloudFormation:** Model and provision all your resources using code (Infrastructure as Code). It's like building your cloud environment with blueprints. 📜
* **AWS OpsWorks:** Automate operations using Chef and Puppet, streamlining configuration management.  Let automation take the wheel! 🤖
* **AWS Service Catalog:** Create, organize, and govern your own curated catalog of AWS products for your organization. It's like your personal AWS app store. 🛍️
* **AWS Marketplace:**  Discover, test, and deploy software that runs on AWS. Find the perfect tools for your needs. 🧰

### Operating Your AWS Environment: Smooth Sailing ⛵

These services are your trusted crew for keeping your AWS environment running smoothly:

* **Amazon CloudWatch:**  Monitor your services through metrics and logs, keeping a watchful eye on your cloud infrastructure.  👀
* **Amazon Config:** Record and evaluate the configurations of your AWS resources, ensuring everything is in order. 
* **AWS CloudTrail:** Tracks all user activity in your AWS account, providing valuable audit trails for security investigations. 🕵️‍♀️
* **AWS Systems Manager:** Optimize performance and security while managing a large fleet of systems. Streamline administration tasks.  
* **Amazon X-Ray:** Analyze and debug applications in production, identifying performance bottlenecks and issues. 🔍

With AWS management and governance services, you can focus on innovation while maintaining control, security, and efficiency across your cloud environment. 

## AWS CloudFormation: Infrastructure as Code 💻🏗️

CloudFormation is a powerful service that lets you provision AWS services, like virtual machines or VPCs, using code.  It&#39;s like magic! ✨  You define what you need in a template, and CloudFormation brings it to life in your AWS environment.

**CloudFormation Templates: Your Infrastructure Blueprints 📝**

CloudFormation Templates are the blueprints for your infrastructure. You can write them in JSON or YAML format, and they define a stack of resources to provision.  It's like creating a recipe for your cloud environment! 

**Benefits of CloudFormation:  Version Control, Automation, and Scale**

CloudFormation offers significant benefits for managing your infrastructure:

* **Version Control:** Because you define your infrastructure as code, you can store it in a version control system like Git and GitHub. This allows you to:
    * Track changes over time, creating a complete history of your infrastructure. 
    * Collaborate with your team on infrastructure deployments. 🤝
* **Automation:** CloudFormation empowers DevOps teams to automate infrastructure creation and resource provisioning in AWS, saving time and effort. 🤖
* **Scale:**  Replicate your infrastructure across multiple AWS accounts and regions with ease. You simply adjust the template parameters for each environment. 🌎

CloudFormation enables you to manage your AWS infrastructure efficiently, consistently, and at scale, making it a valuable tool for modern cloud operations.  

## Amazon CloudWatch: Your All-Seeing Eye in the AWS Cloud 👁️

Amazon CloudWatch is your monitoring and observability powerhouse for AWS. It's like having a 24/7 surveillance system for your cloud environment, giving you a complete view of everything that's happening! 

**CloudWatch: Key Capabilities**

CloudWatch enables you to:

* **Collect Metrics:** Gather data from your AWS services, providing insights into their performance and health. 📊
* **Integrate with AWS Services:**  CloudWatch integrates with over 80 AWS services, providing a unified view of your entire cloud infrastructure.  
* **Pre-Built Metrics:** Leverage a wide range of pre-defined metrics for easy monitoring. 
* **Visualize Data:** View your data in a unified dashboard with customizable charts and graphs. 📈📉
* **Configure Alarms:**  Set up alerts based on metric thresholds, notifying you of potential issues or anomalies. 🚨
* **Centralized Log Management:** Collect and store logs from your AWS resources in a central repository. You can then search, analyze, and troubleshoot issues effectively using CloudWatch Logs Insights. 

**CloudWatch in Action:  Protecting Your EC2 Instance**

Let's say you have an EC2 instance accessed via SSH. You want to know if someone is trying to brute-force their way into your instance.  Here's how CloudWatch can help:

1. **Log Collection:** Send your SSH login logs to CloudWatch Logs. 
2. **Filtering:**  Use CloudWatch Logs Insights to filter and visualize the number of failed login attempts. 
3. **Alerting:** Configure a CloudWatch alarm to trigger a notification if the number of failed login attempts exceeds a certain threshold within a specific time period. 

CloudWatch provides the tools you need to monitor, analyze, and respond to events in your AWS environment, ensuring the health, security, and performance of your applications and infrastructure. 

## Auto Scaling:  Your Elastic Compute Powerhouse  💪📈

Auto scaling empowers you to dynamically adjust the number of your virtual machine instances based on pre-defined conditions. It's like having an elastic workforce for your applications! 

**Scale Up, Scale Down, Optimize ⬆️⬇️**

Auto scaling allows you to:

* **Increase Capacity:** Add more instances during peak demand, ensuring your applications can handle the load. 
* **Decrease Capacity:** Reduce the number of instances when demand is low, saving you money on unnecessary resources.  

**Benefits of Auto Scaling:  Availability, Resilience, and Savings 🎉**

* **High Availability:** Keep your applications running smoothly, even during traffic spikes or unexpected failures. 
* **Fault Tolerance:** Automatically replace unhealthy instances, ensuring your applications remain resilient. 
* **Cost Optimization:** Pay only for the resources you actually need, optimizing your cloud spending. 💰

**How Auto Scaling Works:  A Simple Breakdown**

1. **Auto Scaling Group:** Create an auto scaling group to manage your instances.
2. **Minimum Size:**  Define the minimum number of instances to keep running at all times. 
3. **Desired Capacity:** Specify the optimal number of instances based on your typical workload. 
4. **Maximum Size:**  Set the maximum number of instances your application can scale up to.
5. **Load Balancing:** Use an AWS Load Balancer to automatically distribute traffic across the instances in your auto scaling group, ensuring even load distribution and high availability. 

**Beyond EC2: Auto Scaling for Other Services**

Auto scaling isn&#39;t limited to EC2. Other AWS services like DynamoDB and Aurora also support auto scaling, giving you the flexibility to manage capacity for various types of workloads.

Auto scaling is a key feature of AWS, enabling you to build highly scalable, resilient, and cost-efficient applications. 

## AWS CloudFormation: Building with Templates 🏗️

CloudFormation allows you to provision infrastructure as code, using templates to define the resources you want to deploy.  Let's create an S3 bucket using a CloudFormation template, update it by adding another bucket, and then finally delete the entire stack. 

![](https://static.platzi.com/media/articlases/Images/Screenshot%20at%202022-06-03%2015-03-58.png)

**Understanding the Template: Your Infrastructure Blueprint 📝**

The CloudFormation template we'll use is in JSON format (CloudFormation also supports YAML). Here's the basic structure:

```json
{
  "AWSTemplateFormatVersion": "2010-09-09",  // Version of the CloudFormation template language 
  "Description": "this template does XXXX",  //  A description of what the template does
  "Metadata": {},  // Additional information about the template 
  "Parameters": {},  //  Input values that can be provided when creating or updating the stack
  "Mappings": {},  //  Key-value pairs that can be used to map logical names to physical names or other values
  "Conditions": {},  //  Rules that control whether certain resources are created or properties are assigned based on conditions
  "Transform": {}, //  Specifies transformations to be applied to the template
  "Resources": {}, //  The resources to be provisioned by the template (e.g., S3 buckets, EC2 instances)
  "Outputs": {}  //  Output values that can be returned after the stack is created or updated
} 
```

**Creating the Stack: Bringing Your Template to Life**

1. **CloudFormation Console:** Go to the CloudFormation page in your AWS account.
2. **Create Stack:** Click "Create stack."
3. **Specify Template:** Choose "Upload a template file," and upload the `createstack.json` file. This file defines a single S3 bucket named "platzilab."

   ```json
   {
     "Resources": {
       "platzilab": {
         "Type": "AWS::S3::Bucket"
       }
     }
   }
   ```
![](https://static.platzi.com/media/articlases/Images/Screenshot%20at%202022-06-03%2016-10-52.png)

4. **Stack Details:** Click "Next," choose a name for your stack (e.g., "cfnlab"), and click "Next."
5. **Options:** You can add tags to identify your stack and specify an IAM role (optional). 
6. **Review:**  Leave the default settings and click "Next" to review the configurations. Then click "Create stack." 
7. **Stack Creation:**  You can monitor the stack creation progress, events, and resources being created. The S3 bucket's name will include the stack name, the bucket name you specified in the template, and a random string to avoid duplicate names. 

![](https://static.platzi.com/media/articlases/Images/Screenshot%20at%202022-06-03%2016-23-28.png)

This is the first step in using CloudFormation to manage your infrastructure as code. You can expand upon this template to create more complex environments and automate your deployments. 

