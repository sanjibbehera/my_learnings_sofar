## What is AWS App2Container?
AWS App2Container (A2C) is a command line tool to help you lift and shift applications that run in your on-premises data centers or on virtual machines, so that they run in containers that are managed by Amazon ECS, Amazon EKS, or AWS App Runner.

## How App2Container works
You can use App2Container to generate container images for one or more applications running on Windows or Linux servers that are compatible with the **Open Containers Initiative** (OCI). This includes commercial off-the-shelf applications (COTs).

### App2Container performs the following tasks
- Creates an inventory list for the application server that identifies all running ASP.NET (Windows) and Java applications (Linux) that are candidates to containerize.
- Analyzes the runtime dependencies of supported applications that are running, including cooperating processes and network port dependencies.
- Extracts application artifacts for containerization and generates a Dockerfile.
- Initiates builds for the application container.
- Generates AWS artifacts and optionally deploys the containers on Amazon ECS, Amazon EKS, or AWS App Runner. For example:
  - a CloudFormation template to configure required compute, network, and security infrastructure to deploy containers using Amazon ECS, Amazon EKS, or AWS App Runner.
  - An Amazon ECR container image, Amazon ECS task definitions, or AWS CloudFormation templates for Amazon EKS or AWS App Runner that incorporate best practices for security and scalability of the application by integrating with various AWS services.
  - When deploying directly, App2Container can upload AWS CloudFormation resources to an Amazon S3 bucket, and create a CloudFormation stack.
- Optionally creates a CI/CD pipeline with AWS CodePipeline and associated services, to automate building and deploying your application containers.


### Supported Linux distributions
- Ubuntu
- CentOS
- RHEL
- Amazon Linux

#### Supported Java Frameworks running in Linux
  - Tomcat
  - TomEE
  - JBoss (standalone mode)
  - Weblogic
  - Websphere
  - Spring Boot

#### Supported ASP.NET applications running in Linux
  - .Net Core 3.1
  - .Net 5
  - .Net 6
  - .Net 7
  - .Net 8



