# **VPC — Virtual Private Cloud**

VPC is your private network in AWS. The exam tests VPC design constantly — subnets, routing, security, and connectivity patterns.

## **VPC Fundamentals**

| Component | Description | Key Facts |
| ----- | ----- | ----- |
| VPC | Logically isolated network; spans all AZs in a region | Max 5 VPCs per region (soft limit); CIDR range /16 to /28 |
| Subnet | AZ-specific subdivision of a VPC CIDR block | Public (route to IGW) vs Private (no IGW route). AWS reserves 5 IPs per subnet (first 4 \+ last). |
| Internet Gateway (IGW) | Enables internet access for public subnets; horizontally scaled, HA, no bandwidth limit | One IGW per VPC; attach to VPC, add route in public subnet RT |
| NAT Gateway | Allows PRIVATE subnet instances to initiate outbound internet connections; blocks inbound | Regional HA option (not AZ-resilient); deployed IN public subnet; uses Elastic IP |
| Route Table | Rules directing traffic based on destination CIDR | Each subnet associates with one RT; subnets without explicit association use main RT |
| Security Group (SG) | Stateful virtual firewall at instance level; only ALLOW rules | Stateful \= return traffic auto-allowed. Default: all outbound allowed, all inbound denied. |
| Network ACL (NACL) | Stateless firewall at subnet level; ALLOW and DENY rules | Stateless \= must explicitly allow return traffic (ephemeral ports 1024-65535). Evaluated in order by rule number. |
| VPC Peering | Direct private connection between two VPCs (same or different account/region) | NOT transitive — A↔B and B↔C does NOT mean A↔C. No overlapping CIDRs allowed. |
| VPC Endpoints | Private connection to AWS services without internet | Gateway (S3, DynamoDB — free) vs Interface (most services — hourly cost \+ data transfer) |

| ⚠️ EXAM TRAP: NAT Gateway is NOT highly available across AZs by default. For true HA, deploy one NAT Gateway per AZ and configure each private subnet to route to the NAT Gateway in ITS OWN AZ. |
| :---- |

## **Security Group vs NACL — The Classic Comparison**

| Property | Security Group | Network ACL (NACL) |
| ----- | ----- | ----- |
| Level | Instance (ENI) | Subnet |
| State | STATEFUL — return traffic auto-allowed | STATELESS — must allow both directions |
| Rules | Allow only (whitelist) | Allow AND Deny |
| Evaluation | All rules evaluated together | Rules evaluated in numerical order (lowest first); first match wins |
| Default behavior | Deny all inbound; allow all outbound | Allow all traffic (default VPC NACL) |
| Use case | Primary security control per workload | Additional subnet-level security, blocking specific IPs (DDoS) |

| 💡 TIP: Security Groups can reference other Security Groups by ID (not CIDR). This is powerful: allow inbound from 'sg-webserver' to 'sg-database' without knowing IP addresses. This is the correct pattern for tiered application security. |
| :---- |

## **VPC Connectivity Options**

| Option | Use Case | Key Characteristics |
| ----- | ----- | ----- |
| VPC Peering | Connect 2 VPCs directly | Non-transitive; 1:1 relationship; any account/region; no overlapping CIDR |
| Transit Gateway (TGW) | Hub-and-spoke: connect many VPCs \+ on-prem | Transitive routing; 1 TGW can handle thousands of VPCs; route tables on TGW; share via RAM |
| AWS PrivateLink | Expose service to other VPCs without peering | Service runs in NLB; consumers get Interface Endpoint; unidirectional; doesn't expose full VPC |
| Site-to-Site VPN | Encrypted IPSec tunnel over public internet | Fast to set up (\~hours); variable latency; up to 1.25 Gbps per tunnel |
| Direct Connect (DX) | Dedicated private line from on-prem to AWS | Consistent low latency; 1/10/100 Gbps; no encryption by default; long setup (weeks/months) |
| Direct Connect \+ VPN | Encrypted tunnel over Direct Connect | Best of both: dedicated bandwidth \+ encryption for compliance |
| VPN CloudHub | Hub-and-spoke VPN for multiple on-prem sites | Uses Virtual Private Gateway; sites can communicate through AWS |

| 🧠 MNEMONIC: VPN \= Variable/Virtual (goes over internet, encrypted, variable latency). DX \= Dedicated eXpress (physical line, consistent, no encryption). Need both consistency AND encryption? DX \+ VPN. |
| :---- |

## **VPC Flow Logs**

**What it captures:** IP traffic metadata (not packet contents) for VPC, subnet, or ENI. Goes to CloudWatch Logs, S3, or Kinesis Data Firehose.

**Use cases:** Troubleshoot connectivity issues, security analysis, compliance auditing. Flow logs do NOT capture: DNS traffic, Windows license activation, 169.254.x.x (metadata), DHCP traffic.

---

[< ElastiCache - Caching Strategies](11-elasticache.md) | [Back to README](../README.md) | [Route 53 - DNS and Routing Policies >](13-route53.md)
