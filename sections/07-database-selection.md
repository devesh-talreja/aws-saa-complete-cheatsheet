# **Database Selection Guide**

Choosing the right database is a core SAA skill. The exam gives you a scenario and expects you to match it to the correct DB engine.

| Database | Type | Best For | Key Differentiators |
| ----- | ----- | ----- | ----- |
| RDS (MySQL, Postgres, etc.) | Relational (SQL) | Traditional OLTP, existing SQL apps | Managed; automated backups; Multi-AZ; Read Replicas |
| Aurora | Relational (MySQL/Postgres compatible) | High-performance OLTP, SaaS | 5x faster than MySQL; 6-copy storage across 3 AZs; Aurora Serverless |
| DynamoDB | NoSQL Key-Value \+ Document | High-scale internet apps, gaming, IoT, session data | Single-digit ms at any scale; serverless; global tables |
| ElastiCache (Redis) | In-Memory Cache | Session store, real-time leaderboards, pub/sub, ML feature store | Sub-ms latency; persistence options; cluster mode |
| ElastiCache (Memcached) | In-Memory Cache (simpler) | Simple distributed cache; stateless | No persistence; no replication; multi-threaded |
| Redshift | Columnar Data Warehouse (SQL) | OLAP, BI, analytics on large datasets | Columnar storage; MPP; Redshift Spectrum queries S3 |
| Neptune | Graph | Social networks, fraud detection, knowledge graphs | Gremlin (property graph) \+ SPARQL (RDF) |
| DocumentDB | Document (MongoDB-compatible) | Content management, catalogs, user profiles | MongoDB API compatibility; managed; 6 copies like Aurora |
| Keyspaces | Wide Column (Cassandra-compatible) | IoT, time-series, high-write workloads | Serverless; CQL compatible; pay per request |
| Timestream | Time Series | IoT sensor data, DevOps metrics, telemetry | Built-in time-series analytics; auto-tiering |
| QLDB | Ledger (immutable) | Financial transactions, supply chain audit trail | Cryptographically verifiable; centrally owned |
| OpenSearch Service | Search \+ Analytics | Log analytics, full-text search, dashboards | Elasticsearch API compatible; pairs with Kibana/OpenSearch Dashboards |

---

[< Storage Gateway](06-storage-gateway.md) | [Back to README](../README.md) | [RDS - Relational Database Service >](08-rds.md)
