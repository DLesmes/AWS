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
