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
## CloudWatch
- **CloudWatch Alarms**: Monitor metrics and send notifications or take actions based on thresholds
- **CloudWatch Logs**: Collect and store log files from AWS resources
- **CloudWatch Events**: Respond to state changes in AWS resources
- **CloudWatch Dashboards**: Create customizable dashboards to visualize metrics and logs

# Domain 2: Reliability and Business Continuity
- **Recovery Point Objective (RPO)**: Maximum acceptable amount of data loss measured in time, measured in seconds, minutes, or hours
- **Recovery Time Objective (RTO)**: Maximum acceptable amount of time to restore a system measured in seconds, minutes, or hours
## DR Strategies
- **Backup and Restore**: Strategies to protect data and ensure availability in case of failure.
- **Pilot Light**: Minimal version of an environment is always running in the cloud.
- **Warm Standby**: A scaled-down version of a fully functional environment is always running
- **Multi-site active/active**: Data is accessible from multiple AWS Regions.
## S3 Durability, Availability, and Lifecycle
- **Durability**: 99.999999999% (11 nines) durability
- **Availability**: Variable based on storage class
- **Lifecycle Policies**: Automate the transition of objects between storage classes and the expiration of objects.
## S3 Encryption
- **Server-Side Encryption (SSE)**: Data is encrypted at rest by AWS.
- **Client-Side Encryption**: Data is encrypted by the client before being sent to S3.
- **SSE-S3**: AWS manages the encryption keys.
- **SSE-KMS**: AWS Key Management Service (KMS) manages the encryption keys.
- **SSE-C**: Customer manages the encryption keys.

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

## AWS Organizations and Control Tower
### AWS Organizations
- automated account creation and management
- automated resource provisioning
- improved security b cfreating and enforcing structure
- reduced management overhead
- simmplified auditing for compliance
- centralized biling
- simplified AWS service configuration across accounts
### Service Control Policies (SCPs)
do not aaply to users or roles inthe management account, only to member accounts in an organization
### AWS Control Tower
#### Guardrails

## AWS Certificate Manager (ACM)
- can be used to provision, manage, and deploy SSL/TLS X.509 certificates
- can be used with many AWS services including 
    - Elastic Load Balancing
    - CloudFormation
    - CloudFront
    - Elastic Beanstalk
    - Nitro Enclaves

## Encryption
- **At Rest**: Data is encrypted when stored.
- **In Transit**: Data is encrypted when sent over the network.
- **Symmetric Encryption**: Same key is used for encryption and decryption.
- **Asymmetric Encryption**: Public key is used for encryption, private key for decryption.

## KMS
- **Key Management Service (KMS)**: Managed service for creating and controlling encryption keys.
- **Customer Master Keys (CMKs)**: Primary resources in KMS used to encrypt and decrypt data.

### KMS API and CLI
- **Encrypt**: Encrypts plaintext into ciphertext using a specified CMK.
- **Decrypt**: Decrypts ciphertext back into plaintext using the same CMK.
- **GenerateDataKey**: Generates a data encryption key (DEK) that can be used to encrypt data locally.
- **ReEncrypt**: Re-encrypts ciphertext using a different CMK.
- **DescribeKey**: Provides metadata about a specified CMK.
- **ListKeys**: Lists all CMKs in the account.

## Secrets Manager
## SSM Parameter Store

# Domain 5: Networking and Content Delivery

# Reosources
- [Transitioning objects using Amazon S3 Lifecycle](https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html)
- [CloudWatch metrics that are available for your instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html)
- [Amazon CloudWatch metrics for Amazon EBS](https://docs.aws.amazon.com/ebs/latest/userguide/using_cloudwatch_ebs.html)
- [CloudWatch metrics for your Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html)
- [Monitor CloudWatch metrics for your Auto Scaling groups and instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-cloudwatch-monitoring.html)
- [Using CloudWatch metrics with Lambda](https://docs.aws.amazon.com/lambda/latest/dg/monitoring-metrics.html)
- [Monitoring Storage Gateway](https://docs.aws.amazon.com/storagegateway/latest/vgw/Main_monitoring-gateways-common.html)
- [Amazon CloudWatch metrics for Amazon Aurora](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.AuroraMonitoring.Metrics.html)
- [Types of metrics for CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/programming-cloudwatch-metrics.html)