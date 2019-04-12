# AWS Certified Cloud Practitioner Exam Content Outline

## Cloud Concepts (28%)

### Define the AWS Cloud and its value proposition 
- AWS Cloud: Delivering geographically-distributed IT resources on demand.
- NIST definition of Cloud Computing: “Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.”
- Value Proposition: Trade Capital Expense for Variable Expense (instead of having to invest heavily in data centers and servers before you know how you’re going to use them, you can only pay when you consume computing resources, and only pay for how much you consume).
### Identify aspects of AWS Cloud economics
- Reduce/stop spending money on running and maintaining data centers
- Leverage elasticity to match supply with fluctuating demand
- Only pay when consume computing resources, and only pay for how much you consume
- Continual refinement and improvement of system (optimize over time – can measure, monitor, and improve architecture from data you’ve collected on AWS platform).
### List the different cloud architecture design principles
- Security
- Reliability
- Performance Efficiency
- Cost-Optimization
- Operational Excellence 

<br>

## Security (24%)
### Define the AWS Shared Responsibility model
AWS responsible for SECURITY “OF” THE CLOUD
- Software (AWS Foundation Services): Compute, Storage, Database, Networking
- Hardware / AWS Global Infrastructure: Regions, Availability Zones, Edge Locations

Customer Responsible for SECURITY “IN” THE CLOUD
- Customer Data
- Platforms, Applications, Identity and Access Management
- Operating System, Network & Firewall Configuration 
  - (i) Client-Side Data Encryption and Data Integrity Authentication, (ii) Server-Side Encryption (File System and/or Data), (iii) Networking Traffic Protection (Encryption, Integrity, Identity)


### Define AWS Cloud security and compliance concepts
- No public tours of Data Centers
- Encryption at rest and/or in transit
- AWS CloudTrail captures actions made directly by the user or on behalf of the user by an AWS service (Use cases: compliance, security analysis, data exfiltration detection)
- Application Load Balancer supports direct integration with the Web Application Firewall (WAF)
### Identify AWS access management capabilities 
- Security Groups and NACLs (Network Access Control Lists)
  - By default with Security Groups, no inbound traffic allowed, all outbound traffic allowed
  - NACL rules are applied to all EC2 instances in the associated subnet; security groups are applied on a per-instance basis
- IAM is the AWS user management, authentication, and authorization service (IAM roles a secure way to grant permissions to entities that you trust to access AWS resources)
  - 5 areas of IAM: manage user password, manage access keys, manage signing certificates, delete user, add user to groups
- Identity and Access Management (IAM) Policies: 
   - To manage access in AWS: (i) create a policy defining permissions, (ii) associate policy with an identity or resource
   - AWS supports six types of policies: identity-based policies, resource-based policies, permissions boundaries, Organizations SCPs, ACLs, and session policies
- To enable clients to sign-up and sign-in to your mobile and web app, use Amazon Cognito
- NAT Gateways: You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.
### Identify resources for security support 
- AWS Security Blog

<br>

## Technology (36%)
### Define methods of deploying and operating in the AWS Cloud 
- Access AWS through Management Console, CLI, SDKs
- S3 (object storage) – can use to offload serving of content from your application; with URL-based access, clients can directly fetch data themselves from S3
- VPC – defines an IP-address space
- Elastic Beanstalk – allows quick and simple deployment of your web application; can quickly upload and deploy pre-existing code
- EC2 – can create a webpage during new EC2 instance launch process (see directly below to install an Apache web server (httpd), configure web server to automatically start on boot, activate the Web server, create a simple web page)
```
#!/bin/bash
yum -y install httpd
systemct1 enable httpd
systemct1 start httpd
echo '<html><h1>Hello From Your Web Server!</h1></html>' >
/var/www/html/index.html
```
### Define the AWS global infrastructure 
- Regions: geographic areas that host two or more A-Zs
- Availability Zones: collection of data centers in a specific Region
- Edge Locations: enable quicker content delivery (host a CDN called Amazon CloudFront)
### Identify the core AWS services 
- EC2
   - t2 instance type (free tier) good for running Linux but not enough memory to run Windows OS with these
- EBS 
  - detachable/movable data – can reattach to another EC2 instance
  - network-linked persistent storage volume that you can attach to EC2 instances
  - unformatted because don’t know format until attach it
- S3
  - Supports versioning
  - Can define following actions on objects: Archive Only, Permanently Delete Only, Archive and then Permanently Delete
  - Billed for storage, requests, data transfer
- Amazon S3 Storage Classes:
   - Standard: general-purpose storage of frequently accessed data
   - Infrequent Access (IA): for long-lived but less frequently accessed data
   - Glacier: long-term archive and digital preservation
   - Intelligent-Tiering: unknown or changing access
- Global Infrastructure
- VPC
  - An isolated virtual network on AWS cloud
  - By default, ports are off
  - Subnets within Availability Zone (A-Z).
- Security Groups

- Redshift – fast, simple, cost-effective data warehouse that can extend queries to your data lake
- Aurora – MySQL and PostgreSQL-compatible relational database built for the cloud
- CloudFront – fast, highly secure and programmable content delivery network (CDN)
- CloudFormation – model and provision all of your cloud infrastructure resources
- CloudWatch – complete visibility (monitoring and management) of your cloud resources and applications
- Kinesis – easily collect, process, and analyze video and data streams in real time
- AWS Lambda – run code without thinking about (provisioning or managing) servers; pay only for the compute time you consume
- Route 53 – a highly available and scalable cloud Domain Name System (DNS) web service
- Relational Database Service (RDS) – set up, operate, and scale a relational database in the cloud with just a few clicks.
- Elastic Beanstalk –  an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.
- Simple Notification Service (SNS) – fully managed sub/pub messaging for microservices, distributed systems, and serverless applications
- Simple Queue Services (SQS) – fully managed message queues for microservices, distributed systems, and serverless applications
- CloudTrail – track user activity and API usage  
- DynamoDB – fast and flexible NoSQL database service for any scale 
- AWS Key Management Service (KMS) – easily create and manage keys and control the use of encryption across a wide range of AWS services and in your applications.
- AWS Shield – A managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS.

### Identify resources for technology support 
- Proactive Guidance via Technical Account Manager (TAM)
- Four support plans: basic, developer, business, enterprise

<br>

## Billing and Pricing (12%)
### Compare and contrast the various pricing models for AWS 
- EC2s via on-demand instances, reserved instances, spot (bid) instances
### Recognize the various account structures in relation to AWS billing and pricing 
- Object Storage Class Levels: Min storage duration 30 days (except Glacier – for long-term storage/archiving – which is 90 days) – pay for entire minimum duration even if change mind after first day.
### Identify resources available for billing support
- Account Assistance via AWS Support Concierge

<br>

## Additional Notes
- Software as a Service (SaaS) – end-user applications
- Platform as a Service (PaaS) – remove need for organizations to manage underlying infrastructure (e.g., SQS, SNS, SES, Amazon SQ, Elastic Beanstalk)
- Infrastructure as a Service (IaaS) — basic building blocks for cloud IT; provide access to networking features, computers (virtual or on dedicated hardware), and data storage space (e.g., Regions, Availability Zones, Edge Locations)
- Anything as a Service (XaaS) – Internet of Things (IOT)
<br>

- **Instance store** volumes for your EC2 instance delete root volume configuration when you terminate the instance.

## Sources
- aws.amazon.com websites, docs.aws.amazon.com websites
- qwiklabs.com
- WebAgeSolutions (AWS Practitioner Exam Prep Course)
- AWS Cloud Practitioner Essentials (Second Edition) online exam prep videos
