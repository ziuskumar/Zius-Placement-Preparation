# Introduction to AWS

---

# Introduction

Amazon Web Services (AWS) is the world's leading cloud computing platform. It provides hundreds of on-demand cloud services that help individuals, startups, and enterprises build, deploy, and manage applications without owning physical infrastructure.

Today, millions of customers—including startups, government organizations, and Fortune 500 companies—use AWS to power their applications.

---

# Definition

> **Amazon Web Services (AWS)** is a cloud computing platform provided by Amazon that offers computing, storage, networking, databases, AI, security, analytics, and many other services on a **pay-as-you-go** pricing model.

---

# History of AWS

| Year | Milestone |
|------|-----------|
| 2002 | AWS introduced as web-based services |
| 2006 | EC2 and S3 officially launched |
| 2012 | Rapid expansion of cloud services |
| 2014 | AWS Lambda introduced (Serverless Computing) |
| Present | 200+ cloud services available worldwide |

---

# Why AWS Was Created

Before AWS:

- Companies had to purchase expensive hardware.
- Setting up servers took weeks.
- Scaling applications required buying more servers.
- Small startups couldn't afford large data centers.

AWS solved these problems by allowing anyone to rent computing resources on demand.

---

# Why AWS is Popular

- Largest cloud provider in the world.
- 200+ fully managed services.
- Highly secure infrastructure.
- Global presence with multiple Regions and Availability Zones.
- Pay only for what you use.
- Easy to scale applications.
- Reliable and highly available.

---

# AWS Global Infrastructure (Overview)

AWS infrastructure is organized into:

```
AWS Global Infrastructure

        AWS
         │
 ┌───────┴────────┐
 │                │
Regions       Edge Locations
 │
Availability Zones
```

### Region

A **Region** is a geographical area where AWS has data centers.

Examples:

- Mumbai
- Singapore
- Frankfurt
- London
- Virginia

---

### Availability Zone (AZ)

Each Region contains multiple isolated data centers called Availability Zones.

Example:

Mumbai Region

```
Mumbai Region

├── AZ A
├── AZ B
└── AZ C
```

Applications can be deployed across multiple AZs for high availability.

---

### Edge Location

Edge Locations are used primarily by **CloudFront (CDN)** to cache content closer to users, reducing latency.

---

# AWS Pricing Model

AWS follows a **Pay-As-You-Go** pricing model.

You are charged only for the resources you consume.

Common pricing factors:

- Compute hours (EC2)
- Storage used (S3)
- Database usage (RDS)
- Data transfer
- Requests

---

# Benefits of AWS

- No upfront investment
- High scalability
- High availability
- Global reach
- Strong security
- Automatic scaling
- Disaster recovery support
- Large service ecosystem

---

# Core AWS Service Categories

| Category | Example Services |
|----------|------------------|
| Compute | EC2, Lambda |
| Storage | S3, EBS |
| Database | RDS, DynamoDB |
| Networking | VPC, Route 53, ELB |
| Security | IAM, KMS |
| Monitoring | CloudWatch, CloudTrail |
| Messaging | SQS, SNS |
| Containers | ECS, EKS |
| DevOps | CloudFormation, CodePipeline |

---

# Most Important AWS Services

## EC2 (Elastic Compute Cloud)

Provides virtual servers for running applications.

Example:
- Host a web application.

---

## S3 (Simple Storage Service)

Object storage for images, videos, backups, and files.

Example:
- Store user-uploaded photos.

---

## RDS (Relational Database Service)

Managed SQL databases such as MySQL and PostgreSQL.

Example:
- Store customer information.

---

## DynamoDB

Fully managed NoSQL database.

Example:
- Gaming leaderboards.
- Shopping carts.

---

## Lambda

Run code without managing servers.

Example:
- Resize an uploaded image automatically.

---

## IAM

Manage users, roles, and permissions securely.

---

## VPC

Create an isolated virtual network for AWS resources.

---

## CloudWatch

Monitor applications, logs, and performance metrics.

---

# How AWS Works

```
User
  │
Internet
  │
AWS Cloud
  │
 ├── EC2 (Application)
 ├── S3 (Storage)
 ├── RDS (Database)
 ├── IAM (Security)
 └── CloudWatch (Monitoring)
```

---

# Real-World Example

Suppose you build an online shopping website.

- Users visit your website hosted on **EC2**.
- Product images are stored in **S3**.
- Customer and order details are stored in **RDS**.
- Access is managed using **IAM**.
- Application performance is monitored using **CloudWatch**.
- Traffic increases during a sale, and **Auto Scaling** launches additional EC2 instances automatically.

---

# AWS Free Tier

AWS provides a Free Tier for beginners.

It includes limited usage of services such as:

- EC2
- S3
- Lambda
- RDS
- DynamoDB

This allows users to learn AWS without significant cost (subject to usage limits).

---

# Interview Keywords

- AWS
- Cloud Provider
- EC2
- S3
- IAM
- Lambda
- RDS
- DynamoDB
- VPC
- CloudWatch
- Region
- Availability Zone
- Edge Location
- Pay-As-You-Go
- High Availability
- Scalability

---

# Common Mistakes

❌ AWS is only for storage.

✅ AWS provides compute, networking, databases, AI, analytics, security, monitoring, and much more.

---

❌ Region and Availability Zone are the same.

✅ A Region contains multiple Availability Zones.

---

❌ AWS is free.

✅ AWS offers a Free Tier, but most services are billed based on usage.

---

# Interview Traps

### Q1. What is AWS?

AWS is Amazon's cloud computing platform that provides on-demand IT resources over the Internet with a pay-as-you-go pricing model.

---

### Q2. Why is AWS popular?

- Scalable
- Reliable
- Secure
- Global infrastructure
- Cost-effective
- 200+ managed services

---

### Q3. What is the difference between a Region and an Availability Zone?

- **Region:** A geographic location containing AWS data centers.
- **Availability Zone:** An isolated data center within a Region.

---

### Q4. What is the AWS Free Tier?

A limited free usage plan that helps users learn and experiment with AWS services.

---

### Q5. Name five important AWS services.

- EC2
- S3
- IAM
- RDS
- Lambda

---

# Quick Revision

✅ AWS = Amazon Web Services

✅ World's leading cloud provider

✅ Pay-as-you-go pricing

✅ Global Infrastructure:
- Regions
- Availability Zones
- Edge Locations

✅ Core Services:
- EC2
- S3
- IAM
- RDS
- DynamoDB
- Lambda
- VPC
- CloudWatch

✅ Benefits:
- Scalability
- Reliability
- Security
- Global reach
- High availability

---

# Memory Trick 🧠

Remember the acronym:

**"E S I R D L V C"**

- **E** → EC2
- **S** → S3
- **I** → IAM
- **R** → RDS
- **D** → DynamoDB
- **L** → Lambda
- **V** → VPC
- **C** → CloudWatch

These are the core AWS services most commonly discussed in interviews.

---

# Placement Tips 🎯

For freshers, focus first on understanding:

- AWS Global Infrastructure
- EC2
- S3
- IAM
- RDS
- Lambda
- VPC
- CloudWatch

These services form the foundation for most AWS interview questions and real-world cloud applications.