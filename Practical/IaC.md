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

## CloudFormation StackSets:  Multi-Account Deployments Made Easy 🚀

StackSets extend the power of CloudFormation by enabling you to manage stacks across multiple AWS accounts and regions with a single operation.  It's like having a master control panel for your infrastructure! 🕹️

**StackSets: Key Concepts**

* **Account Types:**  StackSets work with two types of accounts:
    * **Administrator Account:** The central account from which you create and manage StackSets.  👑
    * **Target Accounts:** The accounts where the stacks are actually deployed. 🎯
* **Deployment Source:** You deploy StackSets from the administrator account, which must have appropriate permissions to access the target accounts.
* **Stack Instances:** A stack instance refers to a specific stack deployed within a target account.
* **Parameter Overrides:** You can customize deployments by providing different parameters for different target accounts. This flexibility lets you tailor your infrastructure to each environment.

**StackSets in Action: Deploying Across Multiple Accounts**

StackSets streamline multi-account deployments:

1. **Create a StackSet:** In the administrator account, create a StackSet defining your infrastructure.
2. **Add Target Accounts:** Specify the AWS accounts where you want to deploy the stacks.
3. **Deploy:** Launch the StackSet. CloudFormation automatically creates stack instances in each target account.
4. **Target Account Resources:** The resources defined in your StackSet are created within each target account, providing isolation and independent management.

**Why Use StackSets?**

* **Centralized Management:** Manage infrastructure across multiple accounts and regions from a single location.
* **Consistent Deployments:** Ensure consistent infrastructure configurations across all your environments.
* **Simplified Updates:**  Update your infrastructure across all target accounts with a single operation.
* **Improved Security:**  Enforce security best practices and compliance standards across your organization.

StackSets empower you to manage infrastructure at scale, making it easier to maintain consistency, control costs, and enforce security policies across your AWS organization.

### ☀️[Grant self-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs-self-managed.html)☀️

## CloudFormation Nested Stacks:  Organizing and Simplifying Complex Deployments 📚

**What are Nested Stacks?**

Nested stacks arise from the limitations of CloudFormation. They allow you to break down large, complex stacks into smaller, more manageable ones. Think of it like organizing your infrastructure into logical modules.  

**Why Use Nested Stacks?**

* **Limits:**  Overcome CloudFormation&#39;s limits on resources, mappings, and template size.
* **Granularity:** Manage individual resources or groups of related resources in separate stacks.
* **Order and Dependencies:**  Create dependencies and conditions between stacks, ensuring resources are created in the correct order.
* **Inter-stack Communication:**  Stacks can communicate with each other through outputs, allowing you to pass information between modules.

**CloudFormation Limits:**

* **Mappings:** 100 per stack
* **Resources:** 200 per stack
* **Template Body Size:**
    * 51,200 bytes for `CreateStack`, `UpdateStack`, or `ValidateTemplate` operations
    * 460,800 bytes for templates stored in S3

**When to Use Nested Stacks:**

* **Exceeding Limits:** When you need to create more resources or mappings than CloudFormation allows in a single stack.
* **Improved Granularity:** To manage individual resources or related groups of resources independently.
* **Managing Dependencies:**  To establish dependencies and conditions between different parts of your infrastructure.
* **Enabling Reusability:** To create reusable infrastructure modules that can be shared across projects.

**Example: Single Stack with Nested Stacks**

```yaml
AWSTemplateFormatVersion: 2010-09-09
Resources:
  ApiGateway:
    Type: "AWS::CloudFormation::Stack"
    Properties:
      TemplateURL: https://url/api.yml

  Lambda:
    Type: "AWS::CloudFormation::Stack"
    Properties:
      TemplateURL: https://url/lambda.yml

  Dynamo:
    Type: "AWS::CloudFormation::Stack"
    Properties:
      TemplateURL: https://url/dynamo.yml

  Bucket:
    Type: "AWS::CloudFormation::Stack"
    Properties:
      TemplateURL: https://url/bucket.yml
```

In this example, the main stack defines four nested stacks, each responsible for deploying a different part of the infrastructure (API Gateway, Lambda, DynamoDB, and S3 bucket). Each nested stack is defined in a separate template file, referenced by its `TemplateURL`.

### ☀️[Lab #3: Creating Stack Resources](https://github.com/czam01/cloudformation/blob/master/non-nested/master.yml)☀️

![](https://private-user-images.githubusercontent.com/61529697/390262883-8529210d-9663-4840-9220-50e7e1b8de0f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI2ODIxMTUsIm5iZiI6MTczMjY4MTgxNSwicGF0aCI6Ii82MTUyOTY5Ny8zOTAyNjI4ODMtODUyOTIxMGQtOTY2My00ODQwLTkyMjAtNTBlN2UxYjhkZTBmLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI3VDA0MzAxNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPThiMzcwYjkxNzMxMGY1OTA0MzMwMWI3NzUwZGFlMDBiM2U0YmFkZjk4YjNlYTdiNjhkY2M1YmQyYzBiNjA4NmEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.qg-gixSFUGk-vZYC6b_qucRPt59sSG65wYoKVV2p1MM)

### ☀️[Lab #4: Creating Nested Stack Resources](https://github.com/czam01/cloudformation/tree/master/nested)☀️

![](https://private-user-images.githubusercontent.com/61529697/390262884-614c38eb-b966-4758-aa8a-616aecfbaecf.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI2ODIxMTUsIm5iZiI6MTczMjY4MTgxNSwicGF0aCI6Ii82MTUyOTY5Ny8zOTAyNjI4ODQtNjE0YzM4ZWItYjk2Ni00NzU4LWFhOGEtNjE2YWVjZmJhZWNmLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI3VDA0MzAxNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTUxMWU5MGVmYjg4M2JmY2M1N2FmMzBjYzNhMTZhOGRiMjI3YTI4ZDM0YzRlOWQ2OGQzY2VmNDkzY2U4MTM2OWMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.mtbOmyz4Why9bmKcMMgNIfKs_HJXJ0fif62BAmBdpAs)

## CloudFormation Intrinsic Functions:  Unlocking the Power of Your Templates ✨

Intrinsic functions are like built-in helpers within your CloudFormation templates (YAML or JSON). They allow you to access information about resources, manipulate strings, and perform other useful operations directly within your template.  Let's explore some of the most commonly used intrinsic functions:

### **`!GetAtt` : Retrieving Resource Attributes**

The `!GetAtt` function lets you access attributes of a resource defined in your template.  It's like asking a resource, "Hey, what's your ARN?" or "What's your IP address?"

**Example:**

```yaml
Resources:
  ServerlessResourceName:
    Type: AWS::Serverless::Function
    Properties:
      # ... other properties
      Role: !GetAtt LambdaRoleResourceName.Arn  # Get the ARN of the LambdaRoleResourceName resource

  LambdaRoleResourceName:
    Type: AWS::IAM::Role
    # ... properties for the IAM role
```

### **`!FindInMap` : Dynamic Value Mapping**

The `!FindInMap` function retrieves a value from a mapping defined in the `Mappings` section of your template. This is especially useful for region-specific settings.

**Example:**

```yaml
Mappings:
  RegionMap:  # Define a mapping for different regions
    us-east-1:
      HVM64: "ami-0000"  # AMI ID for us-east-1
    us-west-1:
      HVM64: "ami-1111"  # AMI ID for us-west-1
    eu-west-1:
      HVM64: "ami-2222"  # AMI ID for eu-west-1

Resources:
  ResourceName:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !FindInMap  # Dynamically select AMI based on region
        - RegionMap
        - !Ref 'AWS::Region'  # Get the current region
        - HVM64 
```

### **`!Join` : String Concatenation**

The `!Join` function combines multiple strings into a single string. It's like using the "+" operator for strings, but within your CloudFormation template.

**Example:**

```yaml
!Join [":", ["a", "b", "c"]]  # Results in "a:b:c"
```

### **`!Split` and `!Select` : String Manipulation**

* **`!Split`:** Divides a string into a list of values based on a delimiter.
* **`!Select`:** Selects a specific value from a list.

These functions are often used together to extract parts of a string.

**Example:**

```yaml
# Original string: "OPS:XXXXXXXXX"
# Goal: Extract "XXXXXXXXX"

# Function:
!Select [1, !Split [":", !Ref Cuenta]] 

# Result: "XXXXXXXXX" 
```

These intrinsic functions give you powerful tools to work with data and resources within your CloudFormation templates, enabling more dynamic, flexible, and efficient infrastructure deployments.

### ☀️[Referencia de tipos de recursos y propiedades de AWS](https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html)☀️

### ☀️[CloudFormation Ref & GetAtt cheatsheet](https://theburningmonk.com/cloudformation-ref-and-getatt-cheatsheet/)☀️

### ☀️[Referencia de función intrínseca](https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html)☀️

### **`!Sub` Intrinsic Function: String Substitution in CloudFormation**

**Functionality:**

The `!Sub` function substitutes variables within a string with user-specified input. It&#39;s like a "find and replace" operation for your CloudFormation templates, making them more dynamic and flexible.  It replaces placeholders in a string with values that you provide.

**Composition:**

The basic structure of the `!Sub` function is:

```
String VarName: ValueName
```

Where:

* *String* is the string containing variables to be substituted.
* *VarName* is the name of the variable within the string.
* *ValueName* is the value to substitute for the variable.

**Syntax (3 Versions):**

There are three ways to use the `!Sub` function:

* **Version 1 (JSON):**

```json
{ "Fn::Sub": [String, { Var1Name: Var1Value, Var2Name: Var2Value }]}
```

* **Version 2 (YAML - short form):**

```yaml
Fn::Sub:
  - String
  - { Var1Name: Var1Value, Var2Name: Var2Value }
```

* **Version 3 (YAML - short form with !Sub):**

```yaml
!Sub
  - String
  - { Var1Name: Var1Value, Var2Name: Var2Value }
```

**When to Use `!Sub`:**

Use `!Sub` when you need to replace a value in a string, often with a pseudo parameter. Here are some common pseudo parameters used with `!Sub`:

* **`AWS::AccountId`:** Returns the current AWS account ID.
* **`AWS::NotificationARNs`:** Returns the ARNs of the current stack.
* **`AWS::NoValue`:** Removes a value from the property.
* **`AWS::Partition`:** Returns the partition of a resource (e.g., 'aws', 'aws-cn', 'aws-us-gov').
* **`AWS::Region`:** Returns the current region of the stack.
* **`AWS::StackName`:** Returns the name of the stack.
* **`AWS::StackId`:** Returns the ID of the stack.
* **`AWS::URLSuffix`:** Returns the suffix of a domain (e.g., 'amazonaws.com').


**Example using Pseudo Parameters and User-Defined Variables:**

```yaml
!Sub 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}'
```

In this example:

* `'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}'` is the string with variable placeholders.
* `${AWS::Region}` will be replaced with the current AWS region (e.g., 'us-east-1').
* `${AWS::AccountId}` will be replaced with your AWS account ID.
* `${vpc}` will be replaced with the value of a parameter or resource attribute named 'vpc' in your template.


The `!Sub` function is essential for creating dynamic and reusable CloudFormation templates, enabling you to parameterize your infrastructure and adapt it to different environments easily.

### **`!Ref` [Intrinsic Function: Referencing Parameters and Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)**

**When to Use `!Ref`:**

There are two primary use cases for the `!Ref` function:

* **Case 1: Referencing Parameters:** When you need to use the value of a parameter defined in the `Parameters` section of your template.
* **Case 2: Referencing Resource Properties:** When you want to refer to a property of a resource that is *not* accessible using `!GetAtt`.  This is often used for properties like `AvailabilityZone` or other intrinsic properties.

**Functionality:**

The `!Ref` function returns the value of a parameter or a resource.  It's a way to access values that you've defined elsewhere in your template, making your templates more dynamic and reusable.

**Composition:**

The basic structure is:

```
String VarName: ValueName
```

However, with `!Ref`, you're usually referencing the logical ID of a resource or the name of a parameter directly, so the structure becomes:

```
!Ref logicalName  or  !Ref parameterName
```

**Syntax (3 Versions):**

There are three ways to use the `!Ref` function:

* **Version 1 (JSON):**

```json
{ "Ref": "logicalName" } 
```

* **Version 2 (YAML):**

```yaml
Ref: logicalName
```

* **Version 3 (YAML - short form):**

```yaml
!Ref logicalName
```

**Example: Referencing a Parameter**

```yaml
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  NombreLambda:  # Define a parameter named NombreLambda
    Description: Nombre de la funcion Lambda  # Description for the parameter
    Type: String   # Data type of the parameter

Resources:
  LambdaPlatzi:
    Type: AWS::Serverless::Function
    Properties:
      FunctionName: !Ref NombreLambda  # Reference the NombreLambda parameter
      # ... other properties
```

In this example:

1. We define a parameter called `NombreLambda` of type `String`.  This parameter will be used to provide the name of the Lambda function.
2. In the `Resources` section, we define a Lambda function using SAM syntax (`AWS::Serverless::Function`).
3. For the `FunctionName` property, we use `!Ref NombreLambda` to reference the value provided for the `NombreLambda` parameter.  When the stack is created, CloudFormation will substitute this with the actual value you provide for the parameter.

The `!Ref` function is essential for parameterizing your CloudFormation templates, making them more reusable and adaptable to different environments or configurations. 

### **`!ImportValue` Intrinsic Function: Sharing Data Between Stacks**

**When to Use `!ImportValue`:**

* Call an `Export` from another stack.
* Access an exported property from a different stack.  This enables cross-stack communication and modular infrastructure designs.

**Functionality:**

* `!ImportValue` returns the value of an output exported from another stack. It's a way to share data and configurations between different CloudFormation stacks, enabling you to build more modular and reusable infrastructure components.

**Composition:**

* `!ImportValue` takes a single argument: a reference to the logical name of the exported resource. This logical name should match the name assigned to the output in the exporting stack.

**Syntax (3 Versions):**

* **Version 1 (JSON):**

```json
{ "Fn::ImportValue" : sharedValueToImport }
```

* **Version 2 (YAML):**

```yaml
Fn::ImportValue: sharedValueToImport
```

* **Version 3 (YAML - short form):**

```yaml
!ImportValue sharedValueToImport
```

**Example: Sharing a Database ARN**

Imagine you have two stacks:

* **Stack 1:** Creates a DynamoDB table and exports its ARN (Amazon Resource Name).
* **Stack 2:** Needs to access the DynamoDB table created by Stack 1.

**Stack 1 (Exporting Stack):**

```yaml
Resources:
  MyDynamoDBTable:
    Type: AWS::DynamoDB::Table
    # ... table properties ...

Outputs:
  DynamoDBTableARN:  # Logical name of the output
    Value: !GetAtt MyDynamoDBTable.Arn  # Get the ARN of the DynamoDB table
    Export:
      Name: MySharedDBARN # The name to be used for importing this value in other stacks. Must be unique within a region.
```

**Stack 2 (Importing Stack):**

```yaml
Resources:
  MyLambdaFunction:
    Type: AWS::Serverless::Function
    Properties:
      # ... other properties
      Environment:
        Variables:
          TABLE_ARN: !ImportValue MySharedDBARN # Import the ARN from Stack 1
```

In this example, Stack 2 uses `!ImportValue MySharedDBARN` to retrieve the DynamoDB table ARN exported by Stack 1.  This allows Stack 2 to access the DynamoDB table without needing to recreate it.


The `!ImportValue` function facilitates communication between CloudFormation stacks, allowing you to create reusable modules and manage your infrastructure more effectively.

## **[CloudFormation Conditional Functions](https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-conditions.html)**

These functions enable you to create dynamic templates that adapt to different environments or configurations.

**1. `!And` Function:**

* **Functionality:** Returns `true` if *all* conditions within the function evaluate to `true`. Returns `false` if *any* condition is `false`. It's a logical AND operation.
* **Composition:**
  ```yaml
  !And [condition1, condition2, ... ] 
  ```


**2. `!Or` Function:**

* **Functionality:** Returns `true` if *at least one* condition within the function evaluates to `true`. Returns `false` if *all* conditions are `false`. It's a logical OR operation.
* **Composition:**
  ```yaml
  !Or [condition1, condition2, ...]
  ```

**3. `!If` Function:**

* **Functionality:** This is the core conditional function. It returns one value if a condition is true, and another value if the condition is false.  It's like an "if-else" statement.
* **Composition:**
  ```yaml
  !If [condition_name, value_if_true, value_if_false]
  ```
  Where `condition_name` refers to a condition defined in the `Conditions` section of your template.


**4. `!Equals` Function:**

* **Functionality:** Returns `true` if two values are equal, and `false` if they are not.  Often used within `!And`, `!Or`, or `!If` functions to create more complex conditions.
* **Composition:**
  ```yaml
  !Equals [value_1, value_2]
  ```

**Example: Using !Equals and !If**

```yaml
Conditions:
  IsProduction: !Equals [!Ref EnvironmentType, "production"]  # Condition checks if EnvironmentType parameter is "production"

Resources:
  MyResource:
    Type: AWS::SomeResourceType
    Properties:
      InstanceType: !If [IsProduction, "t3.large", "t2.micro"] # Use a larger instance type for production
```

In this example:

* A condition named `IsProduction` is defined. It uses `!Equals` to compare the value of the `EnvironmentType` parameter with the string "production."
* When creating the `MyResource`, the `InstanceType` property is set based on the `IsProduction` condition. If the environment is production, a `t3.large` instance is used; otherwise, a `t2.micro` instance is used.

These conditional functions enable you to create flexible and dynamic CloudFormation templates that adapt to different scenarios and configurations, streamlining your infrastructure deployments.

### ☀️[Referencia sintáctica de la sección Conditions para las plantillas de CloudFormation](https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/UserGuide/conditions-section-structure.html)☀️

## Advantages of Infrastructure Automation: Level Up Your Cloud Game 🚀

Automating your infrastructure brings a wealth of benefits, boosting efficiency, reliability, and security. Here's why automation is a game-changer:

* **Agilidad (Time Optimization):**  Deploy and manage infrastructure faster, freeing up valuable time for other tasks. ⏱️  No more manual configuration headaches!
* **Control and Integrity (Versioning):**  Manage your infrastructure as code, enabling version control, rollbacks, and a clear audit trail of changes.  Track every modification and maintain complete control over your infrastructure's state. 📝
* **Security (Secrets Encryption):** Securely manage sensitive information like passwords and API keys by encrypting secrets, minimizing the risk of exposure. 🔐
* **Usability (Reusability):** Create reusable infrastructure modules and components that can be easily shared and deployed across projects.  Build once, deploy many! ♻️
* **Error Management and Visibility:**  Gain better visibility into errors and issues during deployments.  Automated processes provide clear logs and feedback, making it easier to identify and resolve problems. 🕵️‍♀️
* **Automatic Rollback:**  If a deployment fails, automation can automatically roll back to a previous stable state, preventing partial deployments and minimizing downtime.  ⏪


Automating your infrastructure is a key best practice for modern cloud operations.  It empowers you to manage your cloud resources efficiently, securely, and at scale. 


## Automating Infrastructure Deployments: A CI/CD Pipeline for the Cloud 🚀

Automating your infrastructure deployments is essential for achieving speed, reliability, and consistency in the cloud. Here's how to build a robust CI/CD pipeline for your infrastructure:

**Key Components and Their Roles:**

* **Error Handling &amp; Traceability:**  Comprehensive logging and monitoring are crucial for identifying and resolving issues during deployments. 🕵️‍♀️
* **Rollback:** Implement automatic rollback mechanisms to revert to a previous stable state in case of errors, minimizing downtime and risk. ⏪
* **AWS CodeCommit:** A fully managed source control service that hosts your infrastructure code (e.g., CloudFormation templates). It provides version control, collaboration features, and a complete audit trail of changes. 
* **AWS CloudFormation:** Define your infrastructure as code, enabling repeatable and consistent deployments. 🏗️
* **AWS CodePipeline:**  Orchestrates the entire deployment process, connecting all the components of your pipeline. It acts as the central control panel for your automated deployments. 
* **AWS CodeBuild:** Compiles code, runs tests, and creates deployment artifacts (e.g., packaged Lambda functions, container images). 
* **External Repositories:** Integrate with external Git repositories like GitHub and GitLab to manage your code and trigger deployments.
* **AWS IAM:** Manage user access and permissions within your pipeline. Ensure that only authorized users and services can access and modify your infrastructure. 🔑
* **Amazon CloudWatch:** Monitor your pipeline's execution, track its status, and gain deep insights into any errors or failures. CloudWatch provides dashboards and alerts for comprehensive visibility. 📈
* **Amazon S3:** Store your deployment artifacts (like packaged application code, container images, or CloudFormation templates) in S3 for easy access and distribution. 📦
* **AWS Secrets Manager:** Securely store and manage sensitive information like passwords, API keys, and database credentials, protecting them from unauthorized access. 🤫
* **AWS KMS (Key Management Service):** Encrypt your data and secrets at rest and in transit, providing an additional layer of security for your deployments. 🛡️

By integrating these components, you can build a fully automated CI/CD pipeline for your infrastructure deployments, enabling fast, reliable, and secure releases.  This automation frees up your team to focus on building and innovating, rather than manually managing infrastructure.

### ☀️[CodeStarSourceConnection for Bitbucket Cloud, GitHub, GitHub Enterprise Server, GitLab.com, and GitLab self-managed actions](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference-CodestarConnectionSource.html)☀️

## **Step-by-Step Infrastructure Deployment Pipeline**

1. **Repo:** This is your code repository (like GitHub, GitLab, or AWS CodeCommit), where your infrastructure code (e.g., CloudFormation templates) is stored. 🐈‍⬛
2. **Source:** This stage fetches the code from your repository and triggers the pipeline.  CodePipeline typically uses CodeCommit, S3, or an external Git repository as the source.
3. **Build:**  This stage often involves tools like CodeBuild to compile code, run tests, and prepare deployment artifacts (e.g., zip files, container images).
4. **Deploy:** This stage deploys your infrastructure.  CloudFormation uses the code from the "Source" stage (likely a CloudFormation template) to create or update your AWS resources.
5. **Outputs:** The deployed resources (represented by S3 bucket, DynamoDB, Lambda function) which could include databases, functions, or storage components.

**Related Components:**

* **Artifacts:**  These are the build outputs produced by the "Build" stage, which are then used by the "Deploy" stage.
* **Monitoring:** This involves monitoring the entire pipeline and deployed resources using services like CloudWatch.


**ANSI-Style Representation**


```
+-----------------------------------------------------------------+
|                                                                 |
|  Infrastructure CI/CD Pipeline                                  |
|                                                                 |
+-----------------------------------------------------------------+
|                                                                 |
|  ┌─────────┐       ┌─────────┐    ┌─────────┐      ┌──────┐     |
|  │  Repo 🐈‍⬛│──────▶│ Source  │───▶│  Build  │─────▶│Deploy│─▶🪣 |
|  └─────────┘       └─────────┘    └─────────┘      └──────┘  📦 |
|                                                              λ  |
|       └────────────────────┬───────────────────────────┘        |
|                            │                                    |
|              ┌─────────┐   │   ┌──────────┐                     |
|              │Artifacts│───────│Monitoring│                     |
|              └─────────┘       └──────────┘                     |
|                                                                 |
+-----------------------------------------------------------------+

  Legend: 🐈‍⬛ = Code Repository,  🪣 = S3, 📦 = DynamoDB, λ = Lambda

  Tools: CodePipeline, CodeBuild, CloudFormation, CloudWatch, S3, IAM, etc.
```



This visual representation provides a clearer picture of the steps and components involved in an automated infrastructure deployment pipeline.  I hope this helps!

### ☀️Lab #6: lambda function deployment☀️
   * [Repository structure for lambda function deployment](https://github.com/czam01/lambda-serverless/blob/master/README.md)
   * [Prerequisites for creating pipeline](https://github.com/czam01/cloudformation/blob/master/codepipeline/aws-codepipeline-prereq.sh)
   * Prerequisite deployment
   * [Creating the pipeline for deploying a lambda function](https://github.com/czam01/lambda-serverless/blob/master/config/buildspec.yml)
   * Verification of resources created in the pipeline

## **Security in CloudFormation Templates**

**Services for Enhanced Security:**

* **Secrets Manager:**  Use Secrets Manager to rotate, manage, and retrieve database credentials, API keys, and other secrets securely.  This prevents hardcoding sensitive information in your templates.
* **Parameter Store:**  Provides secure, hierarchical storage for configuration data and secrets. You can store parameters and retrieve them during stack creation or updates, keeping sensitive information out of your templates.

**Security in Deployments:**

* **Protecting Artifacts:** Ensure your build artifacts (e.g., deployment packages) are stored securely in S3 and protected with appropriate access controls. Avoid storing sensitive information directly within artifacts.
* **Using Repository Tokens:**  Use tokens or access keys from your source code repositories (e.g., GitHub, GitLab) to integrate with your deployment pipeline securely. This avoids hardcoding credentials in your pipeline configuration.

**Example: Using Secrets Manager for a GitHub Token**

```yaml
Configuration:
  Owner: czam01
  PollForSourceChanges: false
  OAuthToken: "{{resolve:secretsmanager:CiToken:SecretString:GitHubToken}}" # Retrieve GitHub token from Secrets Manager
  Repo: !Sub ${AWS::StackName} # Using !Sub for dynamic stack name
  Branch: !Ref BranchRepo
```

In this example:

*  The `OAuthToken` property retrieves the GitHub token from AWS Secrets Manager using the `resolve:secretsmanager` helper function.
* The `CiToken` part likely refers to the name of the secret in Secrets Manager.
*  `SecretString:GitHubToken` specifies that the secret is a string and that the `GitHubToken` field within the secret should be retrieved.
*  This approach avoids embedding the GitHub token directly in the CloudFormation template, improving security.

By following these security practices, you can protect your sensitive information, ensure the integrity of your deployments, and build a more secure cloud infrastructure.

## CloudFormation Troubleshooting: Decoding Stack Statuses 🔎

Understanding CloudFormation stack statuses is crucial for troubleshooting deployment issues.  Here's a breakdown of the common statuses you might encounter:

**Creation:**

* **`CREATE_COMPLETE`:**  ✅ Stack creation completed successfully.  Your resources are now live!
* **`CREATE_IN_PROGRESS`:** 🔄 Stack creation is in progress.  Please wait while your resources are being provisioned.
* **`CREATE_FAILED`:** ❌ Stack creation failed. Check your template for errors, review IAM permissions, and verify parameter values.

**Deletion:**

* **`DELETE_COMPLETE`:** ✅  All resources within the stack have been successfully deleted.  Note that CloudFormation retains stack information for 90 days.
* **`DELETE_FAILED`:** ❌ Resource deletion failed. This might happen if some resources are still in use or have dependencies on other resources.  Check for dependencies and try again.
* **`DELETE_IN_PROGRESS`:** 🔄  Resource deletion is in progress.

**Review:**

* **`REVIEW_IN_PROGRESS`:** ⏳ A change set (a set of proposed changes to your stack) is being created but hasn't been executed yet.

**Rollback (After Create Failure):**

* **`ROLLBACK_COMPLETE`:** ✅  Resources have been successfully deleted after a stack creation failure. The rollback was successful.
* **`ROLLBACK_FAILED`:** ❌ Resource deletion failed during rollback after a stack creation failure. Manual cleanup might be required. 
* **`ROLLBACK_IN_PROGRESS`:** 🔄  Rollback is in progress, deleting resources after a stack creation failure.

**Update:**

* **`UPDATE_COMPLETE`:** ✅ Stack update completed successfully. Your changes have been applied.
* **`UPDATE_COMPLETE_CLEANUP_IN_PROGRESS`:** 🧹  CloudFormation is cleaning up old resources after a successful stack update.
* **`UPDATE_IN_PROGRESS`:** 🔄  Stack update is in progress.
* **`UPDATE_ROLLBACK_COMPLETE`:** ⏪ Stack has been successfully rolled back to its previous state after a failed update.
* **`UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS`:** 🧹 CloudFormation is cleaning up resources after a successful rollback from a failed update.
* **`UPDATE_ROLLBACK_FAILED`:** ❌ The attempt to roll back the stack to its previous state after a failed update has failed. Manual intervention might be necessary. 


By understanding these statuses, you can more effectively troubleshoot and manage your CloudFormation deployments. They give you insight into the progress and outcome of stack operations, allowing you to identify and resolve issues quickly.

