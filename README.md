# ☁️ AWS SAA — Master Cheatsheet & Exam Guide

[![AWS](https://img.shields.io/badge/AWS-SAA--C03-orange?style=flat&logo=amazonaws)](https://aws.amazon.com/certification/certified-solutions-architect-associate/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Sections](https://img.shields.io/badge/Sections-26-green)]()

> **By [Devesh Talreja](https://github.com/devesh-talreja)**

---

## 📖 About These Notes

These notes were created by me during my **AWS Solutions Architect Associate (SAA-C03)** exam preparation. I used them heavily during revision — going through each section multiple times to reinforce concepts, memorize key differences, and drill exam traps.

The content covers **all exam domains** with a focus on what actually matters for the exam: comparison tables, architectural decision points, mnemonics, and exam trap callouts.

> **A note on AI assistance:** I used AI tools to help structure, format, and refine these notes — but the core content, the exam insights, and the revision strategy behind them are entirely from my own study sessions. Think of it as having a smart study partner who helped keep the notes clean and well-organized.

If you're prepping for the SAA exam, feel free to use these notes as your revision companion — that's exactly what they were built for.

---

## 📚 Table of Contents

| # | Section | What's Inside |
|---|---------|--------------|
| 1 | [IAM — Identity & Access Management](sections/01-iam.md) | Users, Groups, Roles, Policies, STS, Permission Boundaries, MFA best practices |
| 2 | [EC2 — Elastic Compute Cloud](sections/02-ec2.md) | Instance families, Purchasing options (On-Demand/Reserved/Spot/Dedicated), ASG, Placement Groups, EBS/EFS/FSx |
| 3 | [AWS Lambda](sections/03-lambda.md) | Execution limits, Concurrency (reserved/provisioned), Triggers, Destinations, Error Handling |
| 4 | [Containers on AWS: ECS, EKS, Fargate](sections/04-containers.md) | ECS vs EKS vs Fargate vs App Runner, ECR, when to use each |
| 5 | [S3 — Simple Storage Service](sections/05-s3.md) | Storage classes, Lifecycle policies, Security layers, Encryption types, CRR/SRR, Performance |
| 6 | [Storage Gateway](sections/06-storage-gateway.md) | S3 File Gateway, FSx File Gateway, Volume Gateway (Cached/Stored), Tape Gateway |
| 7 | [Database Selection Guide](sections/07-database-selection.md) | RDS vs Aurora vs DynamoDB vs Redshift vs Neptune — full decision table |
| 8 | [RDS — Relational Database Service](sections/08-rds.md) | Multi-AZ vs Read Replicas (classic confusion), Backups, PITR |
| 9 | [Aurora — The Exam Favorite](sections/09-aurora.md) | Cluster storage architecture, Serverless v2, Backtrack, Global Database |
| 10 | [DynamoDB — The Serverless NoSQL Giant](sections/10-dynamodb.md) | Partition/Sort keys, LSI vs GSI, DAX, Streams, Global Tables, Transactions, TTL |
| 11 | [ElastiCache — Caching Strategies](sections/11-elasticache.md) | Redis vs Memcached, Lazy Loading, Write-Through, Write-Behind, TTL |
| 12 | [VPC — Virtual Private Cloud](sections/12-vpc.md) | Subnets, IGW, NAT Gateway, SG vs NACL, Peering, Transit Gateway, PrivateLink, Flow Logs |
| 13 | [Route 53 — DNS & Routing Policies](sections/13-route53.md) | All 8 routing policies, Health Checks, Geolocation vs Geoproximity |
| 14 | [CloudFront — Content Delivery Network](sections/14-cloudfront.md) | Origins, OAC, Signed URLs/Cookies, Lambda@Edge vs CF Functions, WAF, Field Encryption |
| 15 | [Elastic Load Balancing — Three Types Compared](sections/15-load-balancing.md) | ALB vs NLB vs GWLB, Advanced ALB routing, Connection Draining |
| 16 | [Messaging & Event-Driven Architecture](sections/16-messaging.md) | SQS (Standard/FIFO), SNS, EventBridge, Kinesis Streams/Firehose/Analytics, MSK, MQ |
| 17 | [Monitoring Stack — CloudWatch, CloudTrail, Config](sections/17-monitoring.md) | Metrics, Logs, Alarms, CloudTrail audit, AWS Config compliance, X-Ray tracing |
| 18 | [Security Services — Know Your Defense Layers](sections/18-security.md) | WAF, Shield, GuardDuty, Inspector, Macie, KMS, CloudHSM, Secrets Manager, Firewall Manager |
| 19 | [Core Architectural Patterns for SAA](sections/19-architectural-patterns.md) | HA Web App, Serverless Pattern, DR strategies (RTO/RPO), Data Lake, Event-Driven, Well-Architected 6 Pillars |
| 20 | [Migration Services](sections/20-migration.md) | DMS + SCT, Application Migration Service, Snowball/Snowmobile, DataSync, Transfer Family |
| 21 | [Analytics Services](sections/21-analytics.md) | Athena, Redshift, EMR, Glue, QuickSight, OpenSearch, Lake Formation |
| 22 | [Application Integration & Orchestration](sections/22-app-integration.md) | Step Functions, AppFlow, API Gateway (REST vs HTTP), AppSync, SWF |
| 23 | [Other Important Services](sections/23-other-services.md) | CloudFormation, CDK, Elastic Beanstalk, SSM, Organizations, Control Tower, Global Accelerator, Outposts |
| 24 | [Most-Confused Services & Concepts](sections/24-common-confusions.md) | Side-by-side: GA vs CloudFront, SQS vs SNS vs Kinesis, EBS vs EFS vs S3, Multi-AZ variations, Cognito Pools |
| 25 | [Exam-Style Practice Questions](sections/25-practice-questions.md) | 10 scenario-based questions across all 4 SAA domains with full explanations |
| 26 | [Summary: Service Selection by Problem Type](sections/26-summary-quick-reference.md) | "I need to store/compute/connect/secure..." quick-pick tables + Key numbers to memorize + Final tips |

---

## 🚀 How to Use These Notes

### For Exam Preparation
1. **First pass:** Go through sections 1–19 in order to build foundational knowledge
2. **Second pass:** Focus on sections 24 (Common Confusions) and 26 (Quick Reference) — these are high-yield for the exam
3. **Practice:** Work through section 25 (Practice Questions) after covering the content
4. **Day before exam:** Review section 26 only — the key numbers table and final tips

### Reading the Callouts
Each section uses consistent callout formatting:
- **⚠️ EXAM TRAP** — The most commonly missed concepts; these directly address wrong answer choices
- **💡 TIP** — Practical exam strategy and "when to use what" guidance
- **🧠 MNEMONIC** — Memory aids for complex comparisons (e.g., "C = CPU crunching" for Compute Optimized)
- **📌 NOTE** — Additional context before answers in practice questions

### Navigation
Every section file has **← prev | README | next →** links at the bottom so you can move through sections without coming back to this page.

---

## ⚠️ Disclaimer

- These are **personal study notes**, not official AWS documentation
- Information is accurate as of **early 2025 (SAA-C03 exam version)**
- AWS services evolve constantly — always cross-check with official AWS docs for the latest details
- These notes are optimized for **exam preparation**, not for production architecture decisions
- Some content is intentionally simplified to aid memorization

---

## 🔗 Official AWS Resources

| Resource | Link |
|----------|------|
| SAA-C03 Exam Guide | [aws.amazon.com/certification/certified-solutions-architect-associate](https://aws.amazon.com/certification/certified-solutions-architect-associate/) |
| AWS Official Documentation | [docs.aws.amazon.com](https://docs.aws.amazon.com/) |
| AWS Well-Architected Framework | [aws.amazon.com/architecture/well-architected](https://aws.amazon.com/architecture/well-architected/) |
| AWS Architecture Center | [aws.amazon.com/architecture](https://aws.amazon.com/architecture/) |
| AWS Whitepapers | [aws.amazon.com/whitepapers](https://aws.amazon.com/whitepapers/) |
| AWS FAQs (exam-relevant) | [aws.amazon.com/faqs](https://aws.amazon.com/faqs/) |
| AWS Free Tier (practice) | [aws.amazon.com/free](https://aws.amazon.com/free/) |

---

## 📂 Repository Structure

```
aws-saa-cheatsheet/
├── README.md                          ← You are here
└── sections/
    ├── 01-iam.md
    ├── 02-ec2.md
    ├── 03-lambda.md
    ├── ...
    └── 26-summary-quick-reference.md
```

---

*Good luck on your AWS SAA exam! ☁️*  
*— Devesh Talreja*
