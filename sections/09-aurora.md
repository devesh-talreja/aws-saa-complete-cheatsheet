# **Aurora — The Exam Favorite**

Aurora is AWS's own cloud-native relational database. It appears frequently because of its unique architecture.

## **Aurora Architecture Highlights**

| Feature | Aurora | Standard RDS |
| ----- | ----- | ----- |
| Storage | Shared cluster volume: 6 copies across 3 AZs, auto-grows 10 GB increments to 128 TB | Single instance storage or gp3/io1 EBS |
| Read Replicas | Up to 15 Aurora Replicas (vs 5 for RDS) | Up to 5 read replicas |
| Failover | \< 30 seconds (usually \< 10 sec) — promotes replica automatically | \~1-2 minutes for Multi-AZ |
| Backtrack | Rewind database to a point in time WITHOUT restore (seconds, up to 72 hrs back) | Not available — must restore from backup to new instance |
| Aurora Serverless v2 | Auto-scales read/write capacity in fractions of ACUs — pay per use | Must choose instance size upfront |
| Global Database | 1 primary region \+ up to 5 secondary read regions; \< 1 sec replication lag; RTO \< 1 min | Cross-region read replicas (higher lag) |

| 💡 TIP: Aurora Global Database for exam: If the question says 'RPO of seconds' or 'RTO under 1 minute' across regions, Aurora Global Database is the answer. It can also be used for local reads to reduce latency globally. |
| :---- |

---

[< RDS - Relational Database Service](08-rds.md) | [Back to README](../README.md) | [DynamoDB - The Serverless NoSQL Giant >](10-dynamodb.md)
