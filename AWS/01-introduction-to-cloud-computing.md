# Introduction to Cloud Computing

---

# Introduction

Cloud Computing is the on-demand delivery of computing resources such as servers, storage, databases, networking, software, and analytics over the Internet without owning physical hardware.

Instead of purchasing expensive servers, organizations rent computing resources from cloud providers like AWS, Microsoft Azure, and Google Cloud Platform (GCP).

---

# Definition

> Cloud Computing is the delivery of IT resources over the Internet with pay-as-you-go pricing.

Users can access computing resources whenever required without managing physical infrastructure.

---

# Why Cloud Computing Exists

Before cloud computing:

- Companies had to purchase expensive servers.
- Hardware maintenance required dedicated teams.
- Scaling applications was difficult.
- Servers often remained idle, wasting money.
- Disaster recovery was expensive.

Cloud computing solves these problems by providing resources on demand.

---

# Traditional IT vs Cloud Computing

| Traditional IT | Cloud Computing |
|---------------|----------------|
| Buy servers | Rent servers |
| High upfront cost | Pay only for usage |
| Manual scaling | Automatic scaling |
| Own data center | Cloud provider manages infrastructure |
| Weeks to deploy | Minutes to deploy |

---

# Characteristics of Cloud Computing

## 1. On-Demand Self Service

Users can provision resources whenever required without human interaction.

Example:
- Launch an EC2 instance in AWS within minutes.

---

## 2. Broad Network Access

Cloud resources are accessible over the Internet from:

- Laptop
- Mobile
- Tablet
- Desktop

---

## 3. Resource Pooling

Cloud providers share physical resources among multiple customers securely.

This is known as **Multi-Tenancy**.

---

## 4. Rapid Elasticity

Resources can automatically increase or decrease based on demand.

Example:

An e-commerce website receives heavy traffic during a sale.

Cloud automatically adds more servers.

After the sale ends:

Extra servers are removed.

---

## 5. Measured Service

Customers pay only for what they use.

Examples:

- Storage Used
- Compute Hours
- Network Usage

---

# How Cloud Computing Works

```
                User
                  │
                  │ Internet
                  ▼
        Cloud Provider (AWS)
                  │
     ┌────────────┼────────────┐
     │            │            │
 Compute      Storage      Database
 (EC2)          (S3)         (RDS)
```

The cloud provider manages:

- Physical servers
- Networking
- Security
- Power
- Cooling
- Hardware maintenance

The customer focuses only on the application.

---

# Service Models

## IaaS (Infrastructure as a Service)

Provider gives:

- Virtual Machines
- Storage
- Networking

Customer manages:

- OS
- Applications
- Runtime

Examples:

- AWS EC2
- Azure VM

---

## PaaS (Platform as a Service)

Provider manages:

- Infrastructure
- Operating System
- Runtime

Customer only deploys code.

Examples:

- AWS Elastic Beanstalk
- Google App Engine

---

## SaaS (Software as a Service)

Complete software is provided through the Internet.

Users simply use the application.

Examples:

- Gmail
- Google Drive
- Microsoft 365
- Dropbox

---

# Comparison

| Feature | IaaS | PaaS | SaaS |
|----------|------|------|------|
| Infrastructure Managed By | Provider | Provider | Provider |
| Operating System | Customer | Provider | Provider |
| Application | Customer | Customer | Provider |
| End User Access | Developers | Developers | Everyone |

---

# Deployment Models

## Public Cloud

Infrastructure owned by cloud provider.

Examples:

- AWS
- Azure
- GCP

---

## Private Cloud

Infrastructure dedicated to a single organization.

Higher security but more expensive.

---

## Hybrid Cloud

Combination of Public and Private Cloud.

Sensitive data stays in private cloud.

Other workloads run on public cloud.

---

# Advantages of Cloud Computing

- Cost Effective
- High Availability
- Scalability
- Flexibility
- Global Reach
- Disaster Recovery
- Automatic Updates
- High Performance

---

# Disadvantages

- Internet dependency
- Vendor lock-in
- Data privacy concerns
- Downtime (rare but possible)

---

# Real-World Example

Suppose you create an online shopping website.

Without Cloud:

- Buy servers
- Install networking
- Maintain hardware
- Handle failures

With AWS:

- Launch EC2 server
- Store images in S3
- Use RDS for database
- Auto Scale during sales
- Pay only for usage

---

# Interview Keywords

- Cloud Computing
- Pay As You Go
- On-Demand
- Elasticity
- Scalability
- Multi-Tenancy
- High Availability
- Fault Tolerance
- Public Cloud
- Private Cloud
- Hybrid Cloud
- IaaS
- PaaS
- SaaS

---

# Scalability vs Elasticity

| Scalability | Elasticity |
|-------------|------------|
| Increase resources manually or automatically | Resources automatically increase and decrease |
| Long-term growth | Short-term demand |
| Example: Add more servers | Example: Auto Scaling during sale |

---

# Common Mistakes

❌ Cloud means only storage.

✅ Cloud provides compute, networking, databases, AI services, analytics, security, and much more.

---

❌ Scalability and Elasticity are the same.

✅ Scalability is handling long-term growth.

✅ Elasticity is handling temporary demand.

---

❌ Cloud is always cheaper.

✅ It is cost-effective only when resources are managed efficiently.

---

# Interview Traps

### Q1. What is Cloud Computing?

Answer:

Cloud Computing is the on-demand delivery of computing resources over the Internet with pay-as-you-go pricing.

---

### Q2. Difference between IaaS, PaaS and SaaS?

IaaS → Infrastructure

PaaS → Platform

SaaS → Software

---

### Q3. What is Elasticity?

Automatic increase or decrease of resources based on workload.

---

### Q4. What is Scalability?

Ability to handle increasing workload by adding resources.

---

### Q5. What are deployment models?

- Public Cloud
- Private Cloud
- Hybrid Cloud

---

# Quick Revision

✅ Cloud = Computing resources over the Internet

✅ Pay only for usage

✅ Five Characteristics:
- On-Demand
- Broad Network Access
- Resource Pooling
- Rapid Elasticity
- Measured Service

✅ Service Models:
- IaaS
- PaaS
- SaaS

✅ Deployment Models:
- Public
- Private
- Hybrid

✅ Major Benefits:
- Scalability
- Elasticity
- High Availability
- Cost Saving
- Global Access

---

# Memory Trick 🧠

### Service Models

```
I → Infrastructure

P → Platform

S → Software
```

Think:

**I Pay Software**

(IaaS → PaaS → SaaS)

---

# Placement Tips 🎯

For SDE and Cloud interviews, always be able to explain:

- Cloud Computing
- IaaS vs PaaS vs SaaS
- Scalability vs Elasticity
- Public vs Private vs Hybrid Cloud
- Pay-as-you-go model

These concepts form the foundation for understanding AWS services like EC2, S3, RDS, Lambda, and more.