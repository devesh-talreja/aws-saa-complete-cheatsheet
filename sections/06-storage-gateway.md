# **Storage Gateway**

Storage Gateway bridges on-premises infrastructure with AWS cloud storage. Critical for hybrid cloud exam scenarios.

| Gateway Type | Protocol | Backend Storage | Use Case |
| ----- | ----- | ----- | ----- |
| S3 File Gateway | NFS / SMB | Amazon S3 | Store files as S3 objects; on-prem apps accessing S3 via file protocol |
| FSx File Gateway | SMB | Amazon FSx for Windows | Cache frequently accessed Windows files on-prem; Windows AD integration |
| Volume Gateway (Cached) | iSCSI block | S3 (primary) \+ local cache | Keep recently accessed data on-prem; rest in S3 — low latency for hot data |
| Volume Gateway (Stored) | iSCSI block | On-prem (primary) \+ S3 async backup | Keep full dataset on-prem; async backup to S3 as EBS snapshots |
| Tape Gateway | iSCSI VTL (Virtual Tape Library) | S3 / Glacier | Replace physical tape with virtual tapes; integrate with Veeam/Commvault |

| 🧠 MNEMONIC: File \= NFS/SMB → S3 | Volume \= Block (iSCSI) | Tape \= VTL. If the question says 'on-prem NFS access to S3' → S3 File Gateway. If it says 'replace physical tape backup' → Tape Gateway. |
| :---- |

| NEXT: SECTION 4 — DATABASES: RDS, AURORA, DYNAMODB & MORE |
| :---: |

---

[< S3 - Simple Storage Service](05-s3.md) | [Back to README](../README.md) | [Database Selection Guide >](07-database-selection.md)
