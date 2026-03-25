# **Analytics Services**

| Service | Purpose | Key Detail |
| ----- | ----- | ----- |
| Athena | Serverless SQL query over S3 | Pay per query ($5/TB scanned); use columnar formats (Parquet/ORC) and partitioning to reduce cost; no infrastructure |
| Redshift | Managed columnar data warehouse (OLAP) | MPP; columnar storage; Redshift Spectrum queries S3 in-place; RA3 nodes decouple compute from storage |
| EMR (Elastic MapReduce) | Managed Hadoop/Spark/Hive/Presto cluster | For large-scale data processing; transient clusters for batch jobs; use Spot for task nodes |
| Glue | Managed ETL \+ Data Catalog | Serverless Spark ETL; Crawlers auto-discover schema; Data Catalog integrates with Athena/Redshift/EMR |
| QuickSight | Serverless BI and visualization | SPICE in-memory engine; ML-powered insights; pay per session; embeddable dashboards |
| OpenSearch Service | Search \+ log analytics | Elasticsearch API compatible; OpenSearch Dashboards (Kibana); anomaly detection; UEBA |
| Lake Formation | Build, secure, govern data lake on S3 | Fine-grained access control on Glue Data Catalog; column/row level security; simplifies data lake setup |

---

[< Migration Services](20-migration.md) | [Back to README](../README.md) | [Application Integration and Orchestration >](22-app-integration.md)
