# AWS CloudOps Engineer - Associate SOA-C03 Notes
# Domains
- **[Domain 1](#domain-1-monitoring-logging-analysis-remediation-and-performance-optimization)**: Monitoring, Logging, Analysis, Remediation, and Performance Optimization (22% of scored content)
- **[Domain 2](#domain-2-reliability-and-business-continuity)**: Reliability and Business Continuity (22% of scored content)
- **[Domain 3](#domain-3-deployment-provisioning-and-automation)**: Deployment, Provisioning, and Automation (22% of scored content)
- **[Domain 4](#domain-4-security-and-compliance)**: Security and Compliance (16% of scored content) 
- **[Domain 5](#domain-5-networking-and-content-delivery)**: Networking and Content Delivery (18% of scored content)

# Fundamentals

## EBS
### Volume Types
- **General Purpose SSD (gp2, gp3)**: Balanced price and performance for a wide variety of workloads.
- **Provisioned IOPS SSD (io1, io2)**: High-performance SSD for I/O-intensive applications.
- **Throughput Optimized HDD (st1)**: Low-cost HDD for frequently accessed, throughput-intensive workloads.
- **Cold HDD (sc1)**: Lowest-cost HDD for less frequently accessed workloads.
- **Magnetic (standard)**: Lowest-cost HDD for infrequently accessed workloads.

## EC2
### Families
- **General Purpose**: T2, T3, T4
- **Compute Optimized**: C5, C6g
- **Memory Optimized**: R5, R6g
- **Storage Optimized**: I3, I3en
- **Accelerated Computing**: P3, P4, G4

## Elasticache
### Use Cases
- sessions
- database caching
- leaderboards
- streaming data dashboards

## S3
Objects consist of the following components:
- **Key**: Unique identifier for the object within a bucket.
- **Value**: The data stored in the object.
- **Metadata**: Additional information about the object (e.g., content type, size).

# Domain 1: Monitoring, Logging, Analysis, Remediation, and Performance Optimization
# Domain 2: Reliability and Business Continuity
# Domain 3: Deployment, Provisioning, and Automation
## Deploying Updates
- **All at once**
- **Rolling**
- **Rolling with additional batch**
    - additional cost
    - good for prod environments
- **Immutable**
    - longest deployment
    - quick rollback in case of failures
    - great for prod environments
- **Blue/Green**
    - swap URLs
    - no downtime
# Domain 4: Security and Compliance
# Domain 5: Networking and Content Delivery