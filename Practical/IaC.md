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

## Infrastructure as Code Tools: A Diverse Landscape 🧰

You have several excellent options for managing your cloud infrastructure as code. Each tool offers its own strengths and caters to different use cases. Let&#39;s break down some of the popular choices:

**1. Terraform (HashiCorp)  🌍**

* **Multi-Cloud Master:**  Terraform excels at multi-cloud deployments, allowing you to manage infrastructure across AWS, Azure, GCP, and more. 
* **Open Source Flexibility:**  Terraform is open source, providing a vibrant community and a wealth of resources. 
* **Enterprise-Ready:**  HashiCorp also offers an enterprise version of Terraform with additional features and support.

**2. Pulumi: Code Your Infrastructure 💻**

* **Leverage Your Coding Skills:**  Pulumi lets you use familiar programming languages (Python, JavaScript, Go, etc.) to define your infrastructure. 
* **Multi-Cloud Support:**  Pulumi also supports deployments across multiple cloud providers. 

**3. Serverless Framework:  Serverless Superpowers ⚡**

* **Serverless Focus:** This framework is specifically designed for deploying serverless architectures, making it easy to work with Lambda functions, DynamoDB, S3, and other serverless components.
* **Behind-the-Scenes CloudFormation:**  For AWS deployments, Serverless Framework uses CloudFormation under the hood. 

**4. SDKs:  Direct Cloud Control 🧰**

* **Cloud-Specific Libraries:** Each cloud provider offers software development kits (SDKs) with libraries for various programming languages.  
* **AWS Boto3:**  For Python developers, Boto3 is the go-to SDK for interacting with AWS services programmatically. 
* **Automation Power:**  SDKs are commonly used in automation scripts and CI/CD pipelines.

**5. AWS CDK:  Cloud Development Kit  🏗️**

* **Developer-Friendly Infrastructure:** AWS CDK allows you to define infrastructure using familiar programming languages. 
* **Abstraction Over CloudFormation:** CDK abstracts away the complexities of CloudFormation templates, making infrastructure code more readable and maintainable.
* **Under the Hood:** CDK generates CloudFormation templates behind the scenes for deployment.

**6. AWS SAM:  Serverless Application Model  ⚡**

* **Serverless Simplified:** AWS SAM is specifically designed for serverless applications on AWS.
* **Streamlined Syntax:**  SAM provides a simplified syntax for defining serverless resources. For example, you define a Lambda function as a "Serverless Function" instead of a "Lambda Function" as you would in CloudFormation.
* **Supported Services:**  SAM works with Lambda, API Gateway, DynamoDB, and other serverless components.

Choosing the right Infrastructure as Code tool depends on your specific needs, preferences, and the complexity of your infrastructure. Consider factors such as multi-cloud support, the desired level of abstraction, and your team&#39;s programming language expertise.

## AWS CloudFormation: Your Infrastructure as Code Powerhouse 💪

**Introduction and Benefits:**

CloudFormation is AWS's powerful Infrastructure as Code (IaC) service. It enables you to model and provision all your AWS resources using code, simplifying and automating your infrastructure management.  

**Here's why CloudFormation is a game-changer:** 🚀

* **Streamlined Deployment:**  Define your infrastructure as code, go through a verification phase, and then deploy seamlessly. You can create templates in either YAML or JSON format.  
* **Comprehensive Services:** CloudFormation offers a range of services, including:
    * **Stacks:**  Logical groupings of related AWS resources.
    * **StackSets:**  Deploy stacks across multiple AWS accounts and regions.
    * **Full AWS Integration:**  Seamless integration with all AWS services.
* **AWS Support:** Get support from AWS for your CloudFormation code, ensuring your deployments go smoothly. (Business support plan required). 🤝
* **Native Integration:** CloudFormation works natively with all AWS services, providing a seamless experience.
* **Visual Designer:** Build your infrastructure visually and preview your existing templates in a user-friendly interface.  
* **Multi-Account Deployment:** Deploy the same infrastructure across multiple AWS accounts, simplifying management and ensuring consistency. 
* **Flexibility:** Create resources dynamically using custom resources, giving you even more control over your infrastructure. 
* **Cost-Effective:** CloudFormation itself is free. You only pay for the resources it provisions. 💰
* **Scalability:** CloudFormation can handle simple to complex architectures, allowing your infrastructure to grow as your needs evolve. 📈
* **Security:**  Deployments are fully secured, with features like key encryption, ensuring your resources are protected. 🔐
* **Stability:** CloudFormation, being a managed service by AWS, offers a high level of SLA (Service Level Agreement), ensuring reliability. 
* **Transactional:**  CloudFormation ensures all resources are created successfully before deploying your application. If there's an error, it performs a rollback, preventing partial deployments. 

**Real-World Success:**

CloudFormation is trusted by industry leaders like:

* FC Barcelona ⚽ 
* Expedia ✈️
* Coinbase 💰
* Nextdoor 🏘️

##  Deconstructing CloudFormation Templates: Your Infrastructure Blueprints 🗺️

**What are CloudFormation Templates?**

CloudFormation templates are text files (written in JSON or YAML format) that define the resources you want to create in your AWS environment. Think of them as detailed instructions for building your cloud infrastructure. 🏗️

**Anatomy of a CloudFormation Template:**

Templates have a specific structure, with several key sections:

* **`AWSTemplateFormatVersion`:**  This specifies the version of the CloudFormation template language. It ensures backward compatibility and lets AWS know how to interpret your template. 
* **`Description`:**  A human-readable description of what your template does. 
* **`Metadata`:** This section can include additional data about your template, like author information, tags, or other metadata. 
* **`Parameters`:** This is where the magic happens! ✨  Define input parameters that can be passed in when you create or update a stack. For example, you can create parameters for:
    * **Resource Names:**  Specify the names of your S3 buckets, EC2 instances, etc.
    * **Instance Types:**  Choose the type of EC2 instance you want to create. 
    * **Lambda Runtime:** Specify the programming language for your Lambda function.
* **`Mappings`:**  Mappings help you dynamically select values based on conditions. For instance, you can use mappings to:
    * **Specify Region-Specific AMIs:**  Choose different Amazon Machine Images (AMIs) based on the region where your stack is being deployed. 

These are just a few of the sections within a CloudFormation template. You can also define resources, outputs, conditions, and more to create complex and flexible infrastructure deployments. 

**Key Takeaways:**

* CloudFormation templates provide a standardized way to define and deploy AWS resources.
* Parameters make your templates reusable and adaptable to different environments.
* Mappings help you create dynamic and flexible deployments based on conditions like regions.

CloudFormation templates are the foundation of infrastructure as code on AWS, allowing you to manage your cloud resources efficiently, repeatably, and at scale. 

```yaml
AWSTemplateFormatVersion: '2021-09-09'

Description: 'This is a sample for the course notes of practical IaC AWS'

Metadata: #NuncaParesDeAprender #esViejoLoSe #loVamosALograr

Parameters:
   myKeryPair:
      Description: Amazon EC2 Key Pair
      Type: “AWS::EC2::KeyPair::KeyName”
   mySubnetIDs:
      Description: Subnet IDs
      Type: “List<AWS::EC2::Subnet::Id>”
   DbSubnetIpBlocks:
      Description: “Comma-delimited list of three CIDR blocks”
      Type: CommaDelimitedList
      Default: “10.0.48.0/24, 10.0.112.0/24, 10.0.176.0/24”
   DBPort:
      Default: 3306
      Description: TCP/IP port for the database
      Type: Number
      MinValue: 1150
      MaxValue: 65535
   DBPwd:
      NoEcho: true
      Description: The database admin account password
      Type: String
      MinLength: 1
      MaxLength: 41
      AllowedPattern: ^[a-zA-z0-9]*$
```

CloudFormation empowers you to manage your AWS infrastructure efficiently, reliably, and at scale, making it a must-have tool for modern cloud operations. 

## [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)

```yaml
AWSTemplateFormatVersion: '2022-02-14'

Description: 'DynamoDB Table creation'

Parameters:
    DynamoAttribute:
        Type: String
    DynamoTableName:
        Type: String
    
Resources:
    DynamoSinceZero:
        Type: AWS::DynamoDB::Table
        DeletionPolicy: Delete
        Properties: 
          AttributeDefinitions: 
            - AttributeName: !Ref DynamoAttribute
              AttributeType: S
          KeySchema: 
            - AttributeName: !Ref DynamoAttribute
              KeyType: HASH
          BillingMode: PAY_PER_REQUEST
          SSESpecification: 
            SSEEnabled: true
          TableName: !Ref DynamoTableName

Outputs:
    DynamoTableName:
        Value: !Ref DynamoSinceZero
        Export:
            Name: DynamoTableName
```

## [Diving Deeper into CloudFormation Templates](https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/UserGuide/template-anatomy.html): Conditions, Transforms, Resources, and Outputs 🧰

We've covered the basics of CloudFormation templates. Now, let's explore some more advanced features:

**`Conditions`:** Decision Points in Your Template

* **Conditional Logic:** `Conditions`  introduce logic into your template, allowing you to control whether certain resources are created or properties are assigned, based on specific conditions.
* **Example:** You might create a condition to check if the environment is "production" and only create certain resources if the condition is true. 

**`Transforms`:** Simplifying Serverless Deployments

* **Serverless Syntax:**  The `Transform`  section allows you to use the simplified syntax of AWS SAM (Serverless Application Model) when deploying serverless applications. 
* **Example:**  You can define a Lambda function using the `AWS::Serverless::Function`  resource type, which is easier to read than the standard  `AWS::Lambda::Function` type in CloudFormation.

**`Resources`:** The Heart of Your Template ❤️

* **Building Blocks:**  The `Resources` section is the most important part of your template. It's where you declare all the resources you want to create (e.g., S3 buckets, EC2 instances, Lambda functions). 
* **Required Field:** The `Resources` section is mandatory in every CloudFormation template. 

**`Outputs`:**  Retrieving Values from Your Stack

* **Returning Data:**  `Outputs`  allow you to define values that can be returned from your stack after it's created. 
* **Accessing Values:** These output values can be used by other stacks or accessed programmatically. 
* **Example:** You could create an output that returns the ARN (Amazon Resource Name) of a DynamoDB table, which can then be used by a Lambda function. 

By using `Conditions`, `Transforms`, `Resources`, and `Outputs` effectively, you can create sophisticated CloudFormation templates that deploy complex, reusable, and flexible infrastructure in your AWS environment. 

### AWS::Lambda::Function 🌞

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Mi primer lambda en platzi

Parameters:
   NombreLambda:
      Description: 'Nombre de la funcion Lambda'
      Type: String
   
   RuntimeLambda:
      Description: Ingresa el runtime de la funcion lambda
      Type: String
      Default: python3.10
      AllowedValues:
         -python3.7
         -python2.7
         -ruby2.5
         -nodejs8.10
         -java8
         -dotnetcore2.1

Resources:
   LambdaPlatzi:
      Type: AWS:Serverless:Function
      Properties: 
         FunctionName: !Ref NombreLambda
         Handler: lambda_function.lambda_handler
         Runtime: !Ref RuntimeLambda
         MemoriSize: 512
         TimeOut: 600
         Role: !GetAtt LambdaRolePlatzi.arn

Outputs: 
   LambdaARN:
      Description: "ARN de la funcion Lambda"
      Value:
         !GetAtt LambdaPlatzi.arn
      Export:
         Name: LambdaPlatziArn
   LambdaName:
      Description: "Nombre de la funcion Lambda"
      Value: 
         !Ref LambdaPlatzi
      Export:
         Name: LambdaPlatziName
```

## Understanding CloudFormation Stacks: Managing Your Cloud Resources as a Team 🏗️

**What is a Stack?**

* **Unified Management:** A stack is a collection of AWS resources that are managed as a single unit. Think of it like a blueprint for a specific part of your cloud infrastructure. 

**Resource Management**

* **All or Nothing:** CloudFormation ensures that all the resources in a stack are either created or deleted together. This helps maintain consistency and prevent partial deployments. 

**What Happens if a Resource Fails to Create?**

* **Rollback:** If any resource in the stack fails to create, CloudFormation automatically rolls back the entire stack, deleting any resources that were successfully created. This ensures that your infrastructure remains in a consistent state. 

**What Happens if I Delete a Stack?**

* **Resource Deletion:** When you delete a stack, all the resources associated with that stack are also deleted.  Be careful! Deleting a stack is a destructive action.

**What is Drift?**

* **Detecting Changes:** Drift occurs when there&#39;s a difference between your CloudFormation template (the desired state of your infrastructure) and the actual state of the resources deployed in AWS. 

**What Can I Identify with Drift?**

* **Resource Mismatch:** Drift detection helps you identify:
    * Resources that have been added outside of CloudFormation.
    * Resources that have been deleted.
    * Resources that have different properties than those defined in your template. 

**Key Benefits of Stacks:**

* **Simplified Management:** Treat your infrastructure as a single unit, making it easier to create, update, and delete. 
* **Consistency:** Ensure that your infrastructure is deployed according to your template, reducing errors and configuration drift.
* **Rollback Protection:** Safeguard against failures by automatically rolling back the entire stack if a resource fails to create. 

### ☀️ [**composition-non-nested-stacks Sample**](https://github.com/czam01/cloudformation/blob/composition-non-nested-stacks/master.yml) ☀️
