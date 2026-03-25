# ☁️ AWS Solutions Architect Associate — Master Cheatsheet

> **By Devesh Talreja**

A comprehensive, exam-ready cheatsheet for the **AWS Solutions Architect Associate (SAA-C03)** certification.

> Complete Service Reference · Comparison Tables · Architectural Patterns · Exam Traps & Mnemonics · Practice Questions · Category Summaries

---

## 📚 Table of Contents

1. [IAM — Identity & Access Management](sections/01-iam.md)
2. [EC2 — Elastic Compute Cloud](sections/02-ec2.md)
3. [AWS Lambda](sections/03-lambda.md)
4. [Containers on AWS: ECS, EKS, Fargate](sections/04-containers.md)
5. [S3 — Simple Storage Service](sections/05-s3.md)
6. [Storage Gateway](sections/06-storage-gateway.md)
7. [Database Selection Guide](sections/07-database-selection.md)
8. [RDS — Relational Database Service](sections/08-rds.md)
9. [Aurora — The Exam Favorite](sections/09-aurora.md)
10. [DynamoDB — The Serverless NoSQL Giant](sections/10-dynamodb.md)
11. [ElastiCache — Caching Strategies](sections/11-elasticache.md)
12. [VPC — Virtual Private Cloud](sections/12-vpc.md)
13. [Route 53 — DNS & Routing Policies](sections/13-route53.md)
14. [CloudFront — Content Delivery Network](sections/14-cloudfront.md)
15. [Elastic Load Balancing — Three Types Compared](sections/15-load-balancing.md)
16. [Messaging & Event-Driven Architecture](sections/16-messaging.md)
17. [Monitoring Stack — CloudWatch, CloudTrail, Config](sections/17-monitoring.md)
18. [Security Services — Know Your Defense Layers](sections/18-security.md)
19. [Core Architectural Patterns for SAA](sections/19-architectural-patterns.md)
20. [Migration Services](sections/20-migration.md)
21. [Analytics Services](sections/21-analytics.md)
22. [Application Integration & Orchestration](sections/22-app-integration.md)
23. [Other Important Services](sections/23-other-services.md)
24. [Most-Confused Services & Concepts](sections/24-common-confusions.md)
25. [Exam-Style Practice Questions](sections/25-practice-questions.md)
26. [Summary: Service Selection by Problem Type](sections/26-summary-quick-reference.md)

---

## 🗂️ Sections at a Glance

| # | Section | Key Topics |
|---|---------|-----------|
| 1 | [IAM](sections/01-iam.md) | Users, Roles, Policies, STS, Permission Boundaries, MFA |
| 2 | [EC2](sections/02-ec2.md) | Instance Families, Purchasing Options, ASG, Placement Groups, EBS/EFS |
| 3 | [Lambda](sections/03-lambda.md) | Limits, Triggers, Concurrency, Destinations, Error Handling |
| 4 | [Containers](sections/04-containers.md) | ECS, EKS, Fargate, ECR, App Runner |
| 5 | [S3](sections/05-s3.md) | Storage Classes, Security, Encryption, Replication, Performance |
| 6 | [Storage Gateway](sections/06-storage-gateway.md) | S3 File, FSx File, Volume (Cached/Stored), Tape Gateways |
| 7 | [Database Selection](sections/07-database-selection.md) | Choosing the right DB: RDS vs DynamoDB vs Redshift vs Neptune etc. |
| 8 | [RDS](sections/08-rds.md) | Multi-AZ vs Read Replicas, Backups, Deletion Protection |
| 9 | [Aurora](sections/09-aurora.md) | Cluster Architecture, Serverless v2, Backtrack, Global Database |
| 10 | [DynamoDB](sections/10-dynamodb.md) | Keys, Consistency, LSI/GSI, DAX, Streams, Global Tables, TTL |
| 11 | [ElastiCache](sections/11-elasticache.md) | Redis vs Memcached, Lazy Loading, Write-Through, Write-Behind |
| 12 | [VPC](sections/12-vpc.md) | Subnets, IGW, NAT, SG vs NACL, Peering, Transit Gateway, Flow Logs |
| 13 | [Route 53](sections/13-route53.md) | 8 Routing Policies, Health Checks, Geolocation vs Geoproximity |
| 14 | [CloudFront](sections/14-cloudfront.md) | CDN, OAC, Signed URLs/Cookies, Lambda@Edge, WAF, Field Encryption |
| 15 | [Load Balancing](sections/15-load-balancing.md) | ALB vs NLB vs GWLB, Advanced Routing, Deregistration Delay |
| 16 | [Messaging](sections/16-messaging.md) | SQS, SNS, EventBridge, Kinesis Streams/Firehose/Analytics, MSK, MQ |
| 17 | [Monitoring](sections/17-monitoring.md) | CloudWatch, CloudTrail, AWS Config, X-Ray, Health Dashboard |
| 18 | [Security](sections/18-security.md) | WAF, Shield, GuardDuty, Inspector, Macie, KMS, CloudHSM, Secrets Manager |
| 19 | [Arch Patterns](sections/19-architectural-patterns.md) | HA Web App, Serverless, DR Strategies, Data Lake, Well-Architected 6 Pillars |
| 20 | [Migration](sections/20-migration.md) | DMS, Application MGN, Snowball/Snowmobile, DataSync, Transfer Family |
| 21 | [Analytics](sections/21-analytics.md) | Athena, Redshift, EMR, Glue, QuickSight, OpenSearch, Lake Formation |
| 22 | [App Integration](sections/22-app-integration.md) | Step Functions, AppFlow, API Gateway, AppSync, SWF |
| 23 | [Other Services](sections/23-other-services.md) | CloudFormation, Beanstalk, SSM, Organizations, Control Tower, Global Accelerator |
| 24 | [Common Confusions](sections/24-common-confusions.md) | Side-by-side comparisons: GA vs CF, SQS vs SNS vs Kinesis, EBS vs EFS vs S3 |
| 25 | [Practice Questions](sections/25-practice-questions.md) | 10 exam-style scenario questions with full explanations |
| 26 | [Quick Reference](sections/26-summary-quick-reference.md) | Service by problem type, Key numbers to memorize, Final tips |

---

## 🚀 How to Use This Guide

- **Jump directly** to any section via the Table of Contents
- Look for **⚠️ EXAM TRAP** callouts — these are the most-missed exam concepts
- Look for **🧠 MNEMONIC** callouts — memory aids for complex topics
- Look for **💡 TIP** callouts — practical exam strategy
- Use the **[Quick Reference](sections/26-summary-quick-reference.md)** the night before your exam
- Each section file has **← prev | README | next →** navigation at the bottom

---

*Good luck on your AWS SAA exam! ☁️*
