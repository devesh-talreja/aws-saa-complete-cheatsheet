# **Summary: Service Selection by Problem Type**

## **I need to store...**

| If you need to store... | Use this service |
| ----- | ----- |
| Files/objects of any size, globally durable | S3 |
| Persistent block storage for one EC2 instance | EBS |
| Shared filesystem across many Linux EC2 instances | EFS |
| Shared filesystem for Windows workloads with Active Directory | FSx for Windows File Server |
| Ultra-high IOPS for HPC or ML workloads | FSx for Lustre |
| Relational data with SQL queries (managed) | RDS (MySQL/Postgres/Oracle/SQL Server/MariaDB) |
| Relational data needing high performance \+ auto-scaling | Aurora |
| Relational data with unknown/variable load (serverless SQL) | Aurora Serverless v2 |
| Non-relational key-value at any scale | DynamoDB |
| In-memory caching for microsecond reads (DynamoDB) | DAX |
| General-purpose in-memory cache with rich data types | ElastiCache for Redis |
| Simple stateless distributed cache | ElastiCache for Memcached |
| Time-series data (IoT, metrics) | Timestream |
| Graph data (social networks, fraud) | Neptune |
| Document data (MongoDB workloads) | DocumentDB |
| Data warehouse for OLAP analytics | Redshift |
| Ledger with cryptographic audit trail | QLDB |
| Search index with full-text search | OpenSearch Service |
| Secrets / credentials with auto-rotation | Secrets Manager |
| Configuration values and non-sensitive secrets | Parameter Store (SSM) |

## 

## **I need to compute...**

| If you need to compute... | Use this service |
| ----- | ----- |
| Virtual machines with full OS control | EC2 |
| Run code without managing servers (\< 15 min tasks) | Lambda |
| Run Docker containers on managed infrastructure | ECS on Fargate |
| Run Docker containers with Kubernetes (managed K8s) | EKS |
| Deploy code without managing servers/containers (PaaS) | Elastic Beanstalk |
| Batch processing at scale (HPC, ML training) | AWS Batch |
| HPC with parallel/distributed computing | EC2 (HPC cluster placement group) \+ FSx for Lustre \+ EFA |
| Run code at CDN edge locations (lightweight) | CloudFront Functions |
| Run code at CDN edge locations (heavier, full Lambda) | Lambda@Edge |
| Scientific computing, genomics, financial risk modeling | AWS Batch or EC2 with P/G instances |

## **I need to connect / network...**

| If you need to... | Use this service |
| ----- | ----- |
| Isolate workloads in a private network | VPC (with private subnets) |
| Give public internet access to EC2 in private subnet | NAT Gateway |
| Connect two VPCs directly (same or different accounts) | VPC Peering |
| Connect many VPCs in a hub-and-spoke model | Transit Gateway |
| Connect on-premises to AWS over internet (encrypted) | Site-to-Site VPN |
| Connect on-premises to AWS with dedicated line | Direct Connect |
| Expose a service to other accounts without full VPC peering | PrivateLink |
| Access S3/DynamoDB from VPC without internet (free) | VPC Gateway Endpoint |
| Access other AWS services from VPC without internet | VPC Interface Endpoint (PrivateLink) |
| Speed up global users to your application | CloudFront or Global Accelerator |
| Route DNS with health checks and traffic policies | Route 53 |
| Distribute HTTP/HTTPS traffic across EC2/containers/Lambda | ALB (Layer 7\) |
| Distribute TCP/UDP traffic with static IPs | NLB (Layer 4\) |
| Inspect traffic through virtual security appliances | GWLB (Layer 3/4) |

## **I need to secure / comply...**

| If you need to... | Use this service |
| ----- | ----- |
| Control who can do what in AWS | IAM (Users, Roles, Policies) |
| Authenticate users for your application | Cognito User Pools |
| Give app users temporary AWS credentials | Cognito Identity Pools |
| Detect threats and anomalous behavior | GuardDuty |
| Find vulnerabilities in EC2/containers/Lambda | Inspector |
| Discover PII in S3 | Macie |
| Protect web apps from attacks (XSS, SQLi) | WAF |
| Protect from DDoS attacks | Shield (Standard free; Advanced paid) |
| Centrally enforce policies across accounts | Firewall Manager |
| Aggregate security findings in one place | Security Hub |
| Audit API calls (who did what, when) | CloudTrail |
| Track resource configuration changes \+ compliance | Config |
| Encrypt data with managed keys | KMS |
| Encrypt data with hardware key isolation (FIPS 140-2 L3) | CloudHSM |
| Manage organization-wide account hierarchy | AWS Organizations \+ SCPs |
| Set up a multi-account landing zone with guardrails | Control Tower |

## 

## 

## 

## **Key Numbers to Memorize**

| Fact | Number |
| ----- | ----- |
| S3 object max size | 5 TB |
| S3 multipart required above | 5 GB (recommended above 100 MB) |
| S3 Standard Availability | 99.99% (4 nines) |
| S3 Standard Durability | 99.999999999% (11 nines) |
| Lambda max timeout | 15 minutes |
| Lambda max memory | 10 GB |
| Lambda default concurrent executions per region | 1,000 (soft limit) |
| SQS max message size | 256 KB (2 GB with Extended Client \+ S3) |
| SQS max retention | 14 days |
| SQS FIFO max throughput | 300 TPS (3,000 with batching) |
| SQS visibility timeout max | 12 hours |
| Kinesis shard write capacity | 1 MB/s or 1,000 records/sec |
| Kinesis shard read capacity | 2 MB/s per consumer (10 MB/s with enhanced fan-out) |
| DynamoDB max item size | 400 KB |
| DynamoDB max partition key per item | 2,048 bytes |
| RDS Multi-AZ failover time | \~1-2 minutes |
| Aurora failover time | \< 30 seconds |
| Aurora storage auto-grow | 10 GB increments up to 128 TB |
| Aurora max read replicas | 15 |
| VPCs per region (default) | 5 (soft limit) |
| Subnets reserved IPs by AWS | 5 (first 4 \+ last 1\) |
| VPC CIDR min/max | /28 (16 IPs) to /16 (65,536 IPs) |
| NAT Gateway max bandwidth | 100 Gbps (scales automatically) |
| EC2 Spread Placement Group max per AZ | 7 instances |
| Route 53 Multi-Value max records | 8 |
| CloudFront edge locations | 400+ |
| Max rules per Security Group | 60 inbound \+ 60 outbound (default) |

## 

## 

## 

## **Final Exam-Day Tips**

| Tip | Detail |
| ----- | ----- |
| Eliminate wrong answers first | SAA is multiple choice. Even if unsure, eliminate 2 wrong options and you have 50/50 odds. |
| 'Most cost-effective' clues | Look for: Spot (batch/fault-tolerant), Reserved (steady-state), S3 lifecycle, Lambda vs EC2, Fargate (no EC2 mgmt), Savings Plans. |
| 'Most operationally efficient' clues | Look for: managed services (RDS over EC2 DB), serverless, automation, IaC (CloudFormation), Systems Manager. |
| 'Highly available' minimum bar | \= Multi-AZ deployment. 2 AZs is HA. 3+ AZs is highly resilient. |
| Security: least privilege first | Always choose the option with minimum required permissions. Roles \> Users. No hardcoded keys ever. |
| Read the question for scope | Is it in one account? One region? Multi-region? Global users? Each scope narrows which services apply. |
| Watch out for 'existing' systems | If the question says 'existing on-prem Oracle/Rabbit/Kafka' → migration service or compatible managed service (MQ, MSK, DMS+SCT). |
| New services \= usually not the answer | SAA targets well-established services. Extremely new launches are rarely the expected answer unless clearly indicated. |

| 🧠 MNEMONIC: The 3 MOST questions in SAA: Most RESILIENT \= Multi-AZ \+ Multi-Region \+ Backups. Most PERFORMANT \= caching \+ right instance type \+ CDN \+ read replicas. Most COST-EFFECTIVE \= Spot/Reserved/Savings Plans \+ right storage tier \+ serverless where applicable. |
| :---- |

***Good luck on your AWS SAA exam\!*** **☁️**

---

[< Exam-Style Practice Questions](25-practice-questions.md) | [Back to README](../README.md)
