# AWS Certification Study Guide

<!-- Table of Contents -->
## Table of Contents
- [AWS Lambda Pricing](#aws-lambda-pricing)
- [Security Services](#security-services)
- [Machine Learning Services](#machine-learning-services)
- [Organization & Billing Management](#organization--billing-management)
- [Data Protection](#data-protection)
- [High Availability Design](#high-availability-design)
- [Connectivity Options](#connectivity-options)
- [Global Infrastructure Benefits](#global-infrastructure-benefits)
- [Database Services](#database-services)
- [Migration Services](#migration-services)
- [Performance Optimization](#performance-optimization)
- [EC2 Purchasing Options](#ec2-purchasing-options)
- [AWS Well-Architected Framework](#aws-well-architected-framework)
- [Notification Services](#notification-services)
- [Dedicated Connectivity](#dedicated-connectivity)
- [AWS Support Plans](#aws-support-plans)
- [Shared Responsibility Model](#shared-responsibility-model)
- [Amazon S3 Characteristics](#amazon-s3-characteristics)
- [Data Encryption](#data-encryption)
- [AWS Programmatic Access](#aws-programmatic-access)

---

## AWS Lambda Pricing

> **Question:** How does AWS charge for AWS Lambda usage once the free tier has been exceeded? (Select TWO.)

**Key Points:**
- ✅ Lambda charges are based on the **number of requests** for your functions
- ✅ Lambda charges depend on the **duration** (execution time) of your code
- ❌ The following do NOT affect Lambda costs:
  - Number of versions of a Lambda function
  - Programming language used
  - Number of functions in an AWS account

*Reference Links:*
- [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda/latest/dg/lambda-foundation.html)

---

## Security Services

> **Question:** Which AWS service identifies security groups that allow unrestricted access to a user's AWS resources?

**Service:** **AWS Trusted Advisor** ✅
- Checks security groups for rules allowing unrestricted access
- Identifies potential vulnerabilities that could lead to hacking, DoS attacks, or data loss

**Other services and their functions:**
- **IAM:** ❌ Manages permissions that control AWS resource access
- **CloudWatch:** ❌ Collects and tracks metrics for AWS resources
- **CloudTrail:** ❌ Provides audit records of API calls

*Reference Links:*
- [Trusted Advisor](https://docs.aws.amazon.com/awssupport/latest/user/trusted-advisor-check-reference.html)
- [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)
- [CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)

---

## Machine Learning Services

> **Question:** A company wants to create a learning application for students. The learning application must give students the option to choose a button to have the text read out loud to them. Which AWS machine learning service will meet this requirement?

**Service:** **Amazon Polly** ✅
- Converts text to speech, allowing text to be read aloud

**Other ML services:**
- **Amazon Transcribe:** ❌ Converts audio to text (speech-to-text)
- **Amazon Translate:** ❌ Provides language translation
- **Amazon Textract:** ❌ Extracts text from scanned documents

*Reference Links:*
- [Amazon Polly](https://docs.aws.amazon.com/polly/latest/dg/what-is.html)
- [Amazon Transcribe](https://docs.aws.amazon.com/transcribe/latest/dg/what-is.html)
- [Amazon Translate](https://docs.aws.amazon.com/translate/latest/dg/what-is.html)
- [Amazon Textract](https://docs.aws.amazon.com/textract/latest/dg/what-is.html)

---

## Organization & Billing Management

> **Question:** Each department within a company has its own independent AWS account and its own payment method. The company needs to centralize departmental governance and consolidate payments. How can the company achieve these objectives by using AWS services or features?

**Solution:** **AWS Organizations** ✅
- Provides centralized governance and billing for multiple AWS accounts

**Alternative services that don't meet requirements:**
- **AWS Cloud Map:** ❌ Creates maps of backend services, doesn't address governance/billing
- **OpsCenter:** ❌ Centralized location for operational work items, doesn't consolidate billing
- **Cost & Usage Reports:** ❌ Consolidates billing reports but doesn't provide central governance

*Reference Links:*
- [AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org.html)
- [AWS Cloud Map](https://docs.aws.amazon.com/cloud-map/latest/dg/what-is-cloud-map.html)
- [OpsCenter](https://docs.aws.amazon.com/systems-manager/latest/userguide/OpsCenter.html)
- [Cost & Usage Reports](https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html)

---

## Data Protection

> **Question:** A user needs to automatically discover, classify, and protect sensitive data stored in Amazon S3. Which AWS service can meet these requirements?

**Service:** **Amazon Macie** ✅
- Automated security assessment that discovers and protects sensitive S3 data

**Other security services:**
- **Amazon Inspector:** ❌ Security assessment for EC2 instances (not S3 data classification)
- **GuardDuty:** ❌ Threat detection service (doesn't perform S3 data classification)
- **Secrets Manager:** ❌ Protects secrets for applications and services (no S3 classification capabilities)

*Reference Links:*
- [Amazon Macie](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)
- [Amazon Inspector](https://docs.aws.amazon.com/inspector/latest/user/what-is-inspector.html)
- [GuardDuty](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html)
- [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)

---

## High Availability Design

> **Question:** What are the advantages of deploying an application with Amazon EC2 instances in multiple Availability Zones? (Select TWO.)

**Advantages:**
- ✅ Prevents single points of failure
- ✅ Improves overall application availability

**What multiple AZs do NOT provide:**
- ❌ Reduced operational costs
- ❌ Lower latency across regions (would need instances in other regions for this)
- ❌ Changes to application load

*Reference Links:*
- [EC2 Regions and Availability Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)

---

## Connectivity Options

> **Question:** A company requires an encrypted connection between the company's on-premises servers and AWS. The connection must use the company's existing internet connection. Which solution will meet these requirements?

**Solution:** **AWS Site-to-Site VPN** ✅
- Creates encrypted network path over existing internet connection

**Other connectivity services:**
- **Direct Connect:** ❌ Dedicated private connection that bypasses the internet
- **Amazon Connect:** ❌ Cloud contact center service, not a network connection
- **CloudFront:** ❌ Content delivery network, not a connectivity solution

*Reference Links:*
- [Site-to-Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html)
- [Direct Connect](https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html)
- [Amazon Connect](https://docs.aws.amazon.com/connect/latest/adminguide/what-is-amazon-connect.html)
- [CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)

---

## Global Infrastructure Benefits

> **Question:** What are benefits of using the AWS Cloud for companies with customers in many countries around the world? (Select TWO.)

**Benefits:**
- ✅ Using Regions around the world improves global performance
- ✅ CloudFront delivers content with low latency via a global edge network

**What's NOT provided:**
- ❌ Amazon Translate doesn't automatically translate third-party website interfaces
- ❌ Amazon Comprehend doesn't translate text
- ❌ Load balancers don't work across regions

*Reference Links:*
- [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
- [AWS Regions](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-regions.html)
- [CloudFront Features](https://aws.amazon.com/cloudfront/features/)
- [CloudFront How It Works](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/HowCloudFrontWorks.html)
- [Amazon Translate](https://docs.aws.amazon.com/translate/latest/dg/how-it-works.html)
- [Amazon Comprehend](https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html)

---

## Database Services

> **Question:** A company requires a relational database on AWS that records new customer orders from a website. Which AWS service or feature will meet this requirement?

**Service:** **Amazon Aurora** ✅
- MySQL/PostgreSQL-compatible relational database built for the cloud
- Combines enterprise performance with open-source cost-effectiveness

**Other services:**
- **Global Accelerator:** ❌ Networking service that improves traffic performance (not a database)
- **DynamoDB:** ❌ NoSQL database (not relational)
- **Amazon EBS:** ❌ Block storage service (not a database itself)

*Reference Links:*
- [Amazon Aurora](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)
- [Global Accelerator](https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html)
- [DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)
- [Amazon EBS](https://docs.aws.amazon.com/ebs/latest/userguide/what-is-ebs.html)

---

## Migration Services

> **Question:** A company has an on-premises Linux-based server with an Oracle database that runs on it. The company wants to migrate the database server to run on an Amazon EC2 instance in AWS. Which service should the company use to complete the migration?

**Service:** **AWS Application Migration Service (MGN)** ✅
- Automated lift-and-shift solution for migrating servers and their applications/databases to EC2

**Other migration-related services:**
- **AWS Database Migration Service (DMS):** ❌ Migrates data only, not the server
- **Migration Hub:** ❌ Plans and tracks migrations but doesn't perform them
- **Application Discovery Service:** ❌ Collects info for migration planning but doesn't execute migration

*Reference Links:*
- [AWS Application Migration Service (MGN)](https://docs.aws.amazon.com/mgn/latest/ug/what-is-application-migration-service.html)
- [AWS Database Migration Service (DMS)](https://docs.aws.amazon.com/dms/latest/userguide/Welcome.html)
- [Migration Hub](https://docs.aws.amazon.com/migrationhub/latest/ug/whatishub.html)
- [Application Discovery Service](https://docs.aws.amazon.com/application-discovery/latest/userguide/what-is-appdiscovery.html)

---

## Performance Optimization

> **Question:** A company is hosting a static website from a single Amazon S3 bucket. Which AWS service will achieve lower latency and high transfer speeds?

**Service:** **Amazon CloudFront** ✅
- Speeds up content distribution by caching at edge locations
- Reduces latency and increases transfer speeds

**Other services:**
- **Elastic Beanstalk:** ❌ Makes application deployment easier but doesn't reduce latency
- **DAX:** ❌ Accelerates DynamoDB (not relevant for S3 websites)
- **Route 53:** ❌ DNS service, but with only one S3 bucket it can't reduce latency

*Reference Links:*
- [CloudFront Introduction and Use Cases](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/IntroductionUseCases.html)
- [Elastic Beanstalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/Welcome.html)
- [DAX](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.html)
- [Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html)
- [Route 53 S3 Routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/RoutingToS3Bucket.html)

---

## EC2 Purchasing Options

> **Question:** Which AWS service allows customers to purchase unused Amazon EC2 capacity at an often discounted rate?

**Service:** **EC2 Spot Instances** ✅
- Provides access to unused EC2 capacity at discounted rates

**Other purchasing options:**
- **Reserved Instances:** ❌ Reserves capacity but isn't unused capacity
- **On-Demand Instances:** ❌ Default option, not discounted
- **Dedicated Instances:** ❌ Run on dedicated hardware, not discounted

*Reference Links:*
- [EC2 Spot Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html)
- [Reserved Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-reserved-instances.html)
- [On-Demand Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-on-demand-instances.html)
- [Dedicated Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html)

---

## AWS Well-Architected Framework

> **Question:** A user deploys an Amazon RDS DB instance in multiple Availability Zones. This strategy involves which pillar of the AWS Well-Architected Framework?

**Pillar:** **Reliability** ✅
- Multi-AZ deployment reduces single points of failure, improving reliability

**Other pillars:**
- **Performance Efficiency:** ❌ Using resources efficiently (multi-AZ doesn't increase performance)
- **Cost Optimization:** ❌ Delivering value at lowest price (multi-AZ increases cost)
- **Security:** ❌ Protecting data and systems (multi-AZ doesn't enhance security)

*Reference Links:*
- [Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/framework/reliability.html)
- [Performance Efficiency Pillar](https://docs.aws.amazon.com/wellarchitected/latest/framework/performance-efficiency.html)
- [Cost Optimization Pillar](https://docs.aws.amazon.com/wellarchitected/latest/framework/cost-optimization.html)
- [Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/framework/security.html)

---

## Notification Services

> **Question:** An application development team needs a solution that sends an alert to an entire development team if a quality assurance test fails on an application. Which AWS service should the application development team use to meet the requirement?

**Service:** **Amazon SNS (Simple Notification Service)** ✅
- Delivers publications to subscribers via text, push notifications, or email

**Other services:**
- **Amazon Connect:** ❌ Cloud contact center (not for notifications)
- **EventBridge:** ❌ Event bus for connecting applications (not for direct notifications)
- **Amazon SQS:** ❌ Message queuing service (not for notifications)

*Reference Links:*
- [Amazon SNS](https://docs.aws.amazon.com/sns/latest/dg/welcome.html)
- [Amazon Connect](https://docs.aws.amazon.com/connect/latest/adminguide/what-is-amazon-connect.html)
- [EventBridge](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html)
- [Amazon SQS](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html)

---

## Dedicated Connectivity

> **Question:** A company wants to establish a consistent and private connection from the company's on-premises data center to the AWS Cloud. Which AWS service will meet these requirements?

**Service:** **AWS Direct Connect** ✅
- Dedicated physical connection via fiber optic cable
- Provides consistent, private connectivity (not shared with other users)

**Other connectivity options:**
- **Client VPN:** ❌ For connecting individual devices, not data centers
- **Site-to-Site VPN:** ❌ Uses the internet (shared, less consistent)

*Reference Links:*
- [AWS Direct Connect](https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html)
- [Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/what-is.html)
- [Site-to-Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html)

---

## AWS Support Plans

> **Question:** What is the MINIMUM AWS Support plan that provides technical support through phone calls?

**Support Plan:** **Business Support** ✅
- Minimum plan that offers phone and chat technical support

**Other support plans:**
- **Enterprise Support:** ❌ Provides phone support but isn't the minimum plan to do so
- **Developer Support:** ❌ Email support only, no phone
- **Basic Support:** ❌ Only for non-technical issues

*Reference Links:*
- [AWS Support Plans](https://aws.amazon.com/premiumsupport/)

---

## Shared Responsibility Model

> **Question:** Which tasks are the customer's responsibility according to the AWS shared responsibility model? (Select TWO.)

**Customer Responsibilities:**
- ✅ Defining IAM users and their access policies
- ✅ Determining access permissions to S3 buckets

**AWS Responsibilities:**
- ❌ Patching Lambda operating systems
- ❌ Patching RDS engines
- ❌ Physical security of data centers

*Reference Links:*
- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [RDS Maintenance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Maintenance.html)
- [AWS Data Center Security](https://aws.amazon.com/compliance/data-center/data-centers/)

---

## Amazon S3 Characteristics

> **Question:** Which of the functionalities are characteristics of Amazon S3? (Select TWO.)

**S3 Characteristics:**
- ✅ Object storage service
- ✅ Durable storage

**What S3 is NOT:**
- ❌ Not a global file system
- ❌ Not a local file store
- ❌ Not a network file system

*Reference Links:*
- [Amazon S3 Overview](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

---

## Data Encryption

> **Question:** Which AWS service should be used to implement encryption in transit?

**Service:** **AWS Certificate Manager (ACM)** ✅
- Creates, stores, and renews SSL/TLS certificates
- Implements encryption in transit using protocols like TLS

**Other services:**
- **AWS RAM:** ❌ For sharing resources across accounts (not for encryption)
- **AWS Shield:** ❌ For DDoS protection (not for encryption)
- **Security Hub:** ❌ For security posture monitoring (not for encryption implementation)

*Reference Links:*
- [AWS Certificate Manager (ACM)](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html)
- [AWS RAM](https://docs.aws.amazon.com/ram/latest/userguide/what-is.html)
- [AWS Shield](https://docs.aws.amazon.com/waf/latest/developerguide/shield-chapter.html)
- [Security Hub](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html)

---

## AWS Programmatic Access

> **Question:** Which credential components are required to gain programmatic access to an AWS account? (Select TWO.)

**Required Credentials:**
- ✅ Access key ID
- ✅ Secret access key

**NOT used for programmatic access:**
- ❌ Primary key (database feature)
- ❌ User ID (for IAM security but not programmatic access)
- ❌ Secondary key (database feature)

*Reference Links:*
- [Access Keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#securing_access-keys)
- [Security Credentials](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html)
- [IAM Users and Root Users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id.html#root-user-vs-iam)
