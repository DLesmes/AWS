# Infraestructure as code notes

## General Architecture
![](https://private-user-images.githubusercontent.com/61529697/380011299-62d0d555-3236-4477-bbf8-dee07847c4a1.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjk4MzA0ODUsIm5iZiI6MTcyOTgzMDE4NSwicGF0aCI6Ii82MTUyOTY5Ny8zODAwMTEyOTktNjJkMGQ1NTUtMzIzNi00NDc3LWJiZjgtZGVlMDc4NDdjNGExLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEwMjUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMDI1VDA0MjMwNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTY1ZWNhMzY2M2ExZDE1YmQ2ZmEzZTAwM2FkMWRiMGVjZGMyMWZkNmY0OGQwZGE2MjBjNzExY2UwMDIwOWU0ZjkmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.6-Kw0oZRBp4kPUnAGHMc-Z4eAYKu6IH4jcfr67iAXdU)

## Infrastructure as Code:  Building Your Cloud with Confidence 🏗️☁️

Deploying infrastructure in the cloud has revolutionized the way we build and manage applications.  Instead of manually configuring servers and services, we can now define our infrastructure as code, automating the process and making it more efficient, reliable, and repeatable.

**Tools for Deploying Infrastructure**

Several popular tools enable Infrastructure as Code (IaC):

* **Terraform (HashiCorp):** A widely used, open-source tool that supports multiple cloud providers, allowing you to define your infrastructure in a declarative language (HCL). 
* **AWS CloudFormation:**  Amazon's native IaC service that lets you define your AWS infrastructure using JSON or YAML templates. 
* **Azure Resource Manager (ARM):** Microsoft Azure's IaC service, using JSON templates to define and deploy infrastructure. 
* **Google Cloud Deployment Manager:**  Google Cloud's IaC service, supporting declarative templates in YAML or Python. 

**Cloud Providers:  Choosing Your Cloud Home**

The leading cloud providers all offer comprehensive IaC capabilities:

* **Amazon Web Services (AWS):** The largest cloud provider with a wide range of services and a mature IaC offering.
* **Microsoft Azure:**  A strong contender with a focus on enterprise solutions and hybrid cloud deployments.
* **Google Cloud Platform (GCP):**  Known for its innovation in AI/ML and data analytics, along with robust IaC tools.

**Key Advantages of Infrastructure as Code**

* **Version Control:** Track changes to your infrastructure code just like you track changes to your application code.  Use Git or other version control systems for collaboration, rollbacks, and a complete audit trail. 
* **Control and Traceability:**  Know exactly who made what changes to your infrastructure and when. IaC provides transparency and accountability. 
* **Efficiency:** Deploy infrastructure to different environments (dev, test, prod) faster and more consistently. No more manual configuration errors! 
* **Automation:**  Automate infrastructure deployments as part of your CI/CD pipeline, accelerating development and release cycles. 
* **Reusability:** Define reusable infrastructure components that can be shared and deployed across projects. 
* **Immutable Infrastructure:** Embrace the concept of immutable infrastructure by deploying fresh environments from your code, eliminating configuration drift and improving consistency. 

Infrastructure as Code is a foundational practice for modern cloud operations, enabling teams to build and manage infrastructure with greater speed, reliability, and control. 
