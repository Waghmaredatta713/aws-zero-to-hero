Day 1 – Introduction to Cloud & AWS (Interview Notes)
1. What is Cloud Computing?
Simple Definition:

Cloud computing means using computing resources like servers, storage, databases, and software over the internet instead of buying and maintaining physical hardware.

In-Depth Explanation:

Earlier, companies had to buy physical servers, install operating systems, maintain power supply, cooling, security, and upgrade hardware. This required a lot of money and manpower.

With cloud computing, all this responsibility is handled by the cloud provider (like AWS). You simply rent the resources you need and pay only for what you use.

Example:

If you want to host a website:

Traditional Way:

Buy a server

Install OS

Configure networking

Maintain hardware

Cloud Way:

Create an EC2 instance

Upload your website

Done in minutes

Real-Life Analogy:

Cloud is like renting a car instead of buying one.
You use it when you need it and don’t worry about maintenance.

2. Benefits of Cloud Computing
1. Cost Effective

You don’t need to buy hardware. You only pay for what you use.

2. Scalability

You can increase or decrease resources anytime.

3. High Availability

Your application can run even if one server fails.

4. Disaster Recovery

Data is backed up in multiple locations.

5. Global Access

You can access your data from anywhere.

Example:

During a sale, Amazon increases servers automatically to handle traffic. After the sale, servers reduce.

3. Types of Cloud
Public Cloud

Owned by providers like AWS, Azure, GCP.

Example: Gmail, Google Drive, AWS EC2

Private Cloud

Used by a single organization.

Example: Banks, government data centers

Hybrid Cloud

Combination of public and private cloud.

Example: Sensitive data in private cloud + website in AWS

4. Cloud Service Models
IaaS (Infrastructure as a Service)

You get virtual servers, storage, and networking.

You manage: OS, apps
Provider manages: Hardware

Example: AWS EC2

PaaS (Platform as a Service)

You focus only on your application code.

Provider manages: OS, runtime, scaling

Example: AWS Elastic Beanstalk

SaaS (Software as a Service)

You directly use the software.

Example: Gmail, Zoom, Dropbox

5. What is AWS?

AWS (Amazon Web Services) is a cloud platform that provides on-demand computing services.

It offers services like:

Compute: EC2, Lambda

Storage: S3, EBS

Database: RDS, DynamoDB

Networking: VPC, Route 53

DevOps: CodePipeline, CloudWatch

Why AWS is Popular:

Pay-as-you-go

Highly secure

Global presence

Highly scalable

6. AWS Global Infrastructure
Region

A region is a geographical area where AWS has data centers.

Example:

Mumbai (ap-south-1)

US East (us-east-1)

Availability Zone (AZ)

An AZ is a physical data center inside a region.

Each region has multiple AZs.

Why AZs Matter:

If one AZ fails, your application still works from another AZ.

7. Region vs Availability Zone
Region	Availability Zone
Geographical area	Data center
Contains multiple AZs	Part of a region
Example: Mumbai	Example: ap-south-1a
8. What is High Availability?

High availability means your application remains accessible even if one server or data center fails.

Example:

If your app runs on 2 servers in 2 AZs, and one AZ fails, the other AZ keeps your app running.

9. What is Scalability?

Scalability is the ability to increase or decrease resources based on demand.

Types:

Vertical Scaling: Increase RAM/CPU

Horizontal Scaling: Add more servers

Example:

During IPL streaming, servers automatically scale.

10. What is Elasticity?

Elasticity is the ability to automatically scale resources up and down.

Example:

Traffic increases → more servers
Traffic decreases → fewer servers

11. What is Fault Tolerance?

Fault tolerance means your system continues to work even when components fail.

12. What is Disaster Recovery?

Disaster recovery is a plan to recover systems after failure.

Example:
Data backup in another region.

13. AWS Shared Responsibility Model

AWS and customer share responsibilities.

AWS Responsible For:

Hardware

Data center

Networking

Physical security

Customer Responsible For:

OS

Applications

Data

IAM

Security groups

Day 1 Architecture Flow

User → Internet → AWS Region → Availability Zone → EC2 → Application