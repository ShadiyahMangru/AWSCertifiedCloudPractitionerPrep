# AWS Certified Cloud Practitioner Exam Content Outline

## Cloud Concepts (28%)

### Define the AWS Cloud and its value proposition 
- AWS Cloud: Delivering geographically-distributed IT resources on demand.
- Value Proposition: Trade Capital Expense for variable expense (instead of having to invest heavily in data centers and servers before you know how you’re going to use them, you can only pay when you consume computing resources, and only pay for how much you consume).
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
- To enable clients to sign-up and sign-in to your mobile and web app, use Amazon Cognito
### Identify resources for security support 
- AWS Security Blog

<br>

## Technology (36%)
### Define methods of deploying and operating in the AWS Cloud 
- Access AWS through Management Console, CLI, SDKs
### Define the AWS global infrastructure 
- Regions
- Availability Zones
- Edge Locations
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

## Additional Notes:
- Software as a Service (SaaS)
- Platform as a Service (PaaS) – SQS, SNS, SES, Amazon SQ, Elastic Beanstalk
- Infrastructure as a Service (IaaS)—e.g., Regions, Availability Zones, Edge Locations
- Anything as a Service (XaaS) – Internet of Things (IOT)

<br>

- **NIST definition of Cloud Computing:** “Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.”

- **AWS KMS:** AWS Key Management Service (KMS) makes it easy for you to create and manage keys and control the use of encryption across a wide range of AWS services and in your applications.

- **NAT Gateways:** You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.

- **Instance store** volumes for your EC2 instance delete root volume configuration when you terminate the instance.

- **Amazon S3 Storage Classes:** 
   - Standard: general-purpose storage of frequently accessed data
   - Infrequent Access (IA): for long-lived but less frequently accessed data
   - Glacier: long-term archive and digital preservation
   - Intelligent-Tiering: unknown or changing access

- **Identity and Access Management (IAM) Policies:** You manage access in AWS by creating policies and attaching them to IAM identities (users, groups of users, or roles) or AWS resources. A policy is an object in AWS that, when associated with an identity or resource, defines their permissions. AWS evaluates these policies when a principal entity (user or role) makes a request. Permissions in the policies determine whether the request is allowed or denied. Most policies are stored in AWS as JSON documents. AWS supports six types of policies: identity-based policies, resource-based policies, permissions boundaries, Organizations SCPs, ACLs, and session policies.
