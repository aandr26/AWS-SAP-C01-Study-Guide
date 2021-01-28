# AWS Certified Solutions Architect - Professional Exam Guide

## About

This guide serves to help the user pass the AWS Certified Solutions Architect - Professional exam.

It generally follows the great course by Adrian Cantrill [AWS Certified Solutions Architect - Professional](https://learn.cantrill.io/p/aws-certified-solutions-architect-professional) course, but includes some additional content that will supplement.

--------------------------------

### Table of Contents

#### AWS Essentials

* [Disaster Recovery: RPO and RTO](./docs/1_AWS_Essentials/Disaster_Recovery_RPO_TRO.md)
* [High Availability, Fault Tolerance and Disaster Recovery](./docs/1_AWS_Essentials/High-Availability_Fault-Tolerance_Disaster-Recovery.md)
* [Regions, Availability Zones, and Edge Locations](./docs/1_AWS_Essentials/Regions_AZs_Edge-Infrastructure.md)
* [Data Persistence](./docs/1_AWS_Essentials/Data_Persistence.md)

--------------------------------

#### AWS Accounts

* **Management and Access:**
  * [IAM Overview](./docs/2_Accounts/2a_AWS_Identity_Basics/IAM_Overview.md)
  * [Identity and Resource Policies Overview](./docs/2_Accounts/2a_AWS_Identity_Basics/Identity_and_Resource_Policies.md)
  * [IAM Roles and Temporary Security Credentials](./docs/2_Accounts/2a_AWS_Identity_Basics/IAM_Roles_and_Temporary_Credentials.md)
  * [Cross-Account Access: Resource Permissions vs. Cross-Account Roles](./docs/2_Accounts/2a_AWS_Identity_Basics/Cross-Account_Access.md)
  * [AWS Accounts and AWS Organizations](./docs/2_Accounts/2b_Account_Management/Accounts_Organizations.md)
  * [AWS Config](./docs/2_Accounts/2b_Account_Management/Config.md)
  * [AWS Service Catalog](./docs/2_Accounts/2b_Account_Management/Service_Catalog.md)
  * [Billing](./docs/2_Accounts/2c_Billing_Models/Billing.md)

* **Advanced Identity and Permissions in AWS:**
  * [IAM Permission Boundaries](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/IAM_Permission_Boundaries.md)
  * [Identity Federation](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/Identity_Federation.md)
  * [Policy Evaluation Logic](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/Policy_Evaluation_Logic.md)
  * [Resource Access Manager](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/Resource_Access_Manager.md)

--------------------------------

#### Networking

* **Essentials:**
  * [VPC Basics](./docs/3_Networking/3a_VPC_Essentials/VPC_Basics.md)
  * [VPC Routing](./docs/3_Networking/3a_VPC_Essentials/VPC_Routing.md)
  * [Network Access Control Lists](./docs/3_Networking/3a_VPC_Essentials/NACLs.md)
  * [Security Groups](./docs/3_Networking/3a_VPC_Essentials/Security_Groups.md)
  * [Private vs Public Subnets, Internet Gateways, IP Addressing](./docs/3_Networking/3a_VPC_Essentials/Pub_vs_Priv_Subnets_IGW_IP_Addressing.md)
  * [Egress-Only Gateway](./docs/3_Networking/3a_VPC_Essentials/Egress-Only_Gateways.md)
  * [VPC Flow Logs](./docs/3_Networking/3a_VPC_Essentials/VPC_Flow_Logs.md)
  * [DNS](./docs/3_Networking/3a_VPC_Essentials/DNS_in_VPC.md)

* **Advanced VPC Networking:**
  * [VPC Endpoints](./docs/3_Networking/3b_Advanced_VPC_Networking/VPC_Endpoints.md)
  * [VPC Peering](./docs/3_Networking/3b_Advanced_VPC_Networking/VPC_Peering.md)
  * [VPNs](./docs/3_Networking/3b_Advanced_VPC_Networking/VPNS.md)
  * [Direct Connect](./docs/3_Networking/3b_Advanced_VPC_Networking/Direct_Connect.md)
  * [Private Link](./docs/3_Networking/3b_Advanced_VPC_Networking/Private_Link.md)
  * [Advanced VPC Structure](./docs/3_Networking/3b_Advanced_VPC_Networking/VPC_Structure.md)

--------------------------------

#### Security

* **Account and Service Security:**
  * [Key Management Service (KMS)](./docs/4_Security/4a_Account_Service_Security/Key_Management_Service_KMS.md)
  * [CloudHSM](./docs/4_Security/4a_Account_Service_Security/CloudHSM.md)
  * [Certificate Manager (ACM)](./docs/4_Security/4a_Account_Service_Security/Certificate_Manager_ACM.md)
  * [Directory Service](./docs/4_Security/4a_Account_Service_Security/Directory_Service.md)
  * [AWS Secrets Manager](./docs/4_Security/4a_Account_Service_Security/Secrets_Manager.md)

* **Network Security:**
  * [WAF and Shield](./docs/4_Security/4b_Network_Security/WAF_Shield.md)
  * [GuardDuty](./docs/4_Security/4b_Network_Security/GuardDuty.md)
  
--------------------------------

#### Compute

* **EC2:**
  * [EC2 Concepts](./docs/5_Compute/5a_EC2/EC2_Concepts.md)
  * [Creating and Using AMIs](./docs/5_Compute/5a_EC2/Creating_Using_AMIs.md)
  * [Virtualization and EC2 Instance Type: Deep Dive](./docs/5_Compute/5a_EC2/Virtualization_EC2_Deep_Dive.md)
  * [EC2 Storage and Snapshots](./docs/5_Compute/5a_EC2/EC2_Storage_and_Snapshots.md)
  * [EC2 Instance Profiles and Roles](./docs/5_Compute/5a_EC2/EC2_Instance_Roles.md)
  * [HPC and Placement Groups](./docs/5_Compute/5a_EC2/HPC_Placement_Groups.md)
* **Containers:**
  * [ECS Architecture](./docs/5_Compute/5b_Containers/ECS_Architecture.md)
  * [ECS Security](./docs/5_Compute/5b_Containers/ECS_Security.md)
* **Serverless:**
  * [Serverless and Event-Driven Architectures](./docs/5_Compute/5c_Serverless/Serverless_Event-Driven_Architectures.md)
  * [Lambda Layers](./docs/5_Compute/5c_Serverless/Lambda_Layers.md)
  * [API Gateway](./docs/5_Compute/5c_Serverless/API_Gateway.md)
* **Workspaces:**
  * [Workspaces Overview](./docs/5_Compute/5d_Workspaces/Workspaces_Overview.md)

--------------------------------

#### Scaling and Resilience

* **Scaling Architecture:**
  * [AWS Service Resilience](./docs/6_Scaling_and_Resilience/6a_Scaling_Architectures/AWS_Service_Resilience.md)
  * [Stateless Architectures](./docs/6_Scaling_and_Resilience/6a_Scaling_Architectures/Stateless_Architectures.md)
  * [Deciding between Spot and Reserved Instances](./docs/6_Scaling_and_Resilience/6a_Scaling_Architectures/Deciding_between_Spot_Reserved_Instances.md)
  * [Implementing Auto Scaling Groups (ASGs)](./docs/6_Scaling_and_Resilience/6a_Scaling_Architectures/Implementing_ASG.md)
  * [Elastic Load Balancers](./docs/6_Scaling_and_Resilience/6a_Scaling_Architectures/ELB.md)
* **CloudFront Essentials:**
  * [CloudFront Architecture](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/CloudFront_Architecture.md)
  * [Creating and Working with Distributions](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/Creating_and_Working_with_Distributions.md)
  * [Working with Custom Origins](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/Custom_Origins.md)
  * [CloudFront and Security](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/CloudFront_Security.md)
  * [Optimizing Caching](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/Optimizing_Caching.md)
  * [Lambda@Edge](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/Lambda_Edge.md)
  * [Logging, Reporting, and Monitoring](./docs/6_Scaling_and_Resilience/6b_CloudFront_Essentials/Logging_Reporting_Monitoring.md)
* **Route 53:**
  * [Route 53 Architecture](./docs/6_Scaling_and_Resilience/6c_Route53/Route53_Architecture.md)
  * [Advanced Route 53 Concepts](./docs/6_Scaling_and_Resilience/6c_Route53/Advanced_Route53_Concepts.md)

--------------------------------

#### Storage

* **Object Storage: Amazon Simple Storage Service (S3):**
  * [S3 Architecture](./docs/7_Storage/7a_S3/S3_Architecture.md)
  * [S3 Storage Tiers, Intelligent-Tiering, and Lifecycle Policies](./docs/7_Storage/7a_S3/S3_Storage_Tiers_Intelligent-Tiering_Lifecycle_Policies.md)
  * [Versioning and Locking](./docs/7_Storage/7a_S3/S3_Versioning_and_Locking.md)
  * [Controlling Access to S3 Buckets](./docs/7_Storage/7a_S3/S3_Controlling_Access.md)
  * [Cross-Region Replication](./docs/7_Storage/7a_S3/S3_Cross-Region_Replication.md)
  * [Object Encryption](./docs/7_Storage/7a_S3/S3_Object_Encryption.md)
  * [Optimizing S3 Performance](./docs/7_Storage/7a_S3/S3_Optimizing_Performance.md)
  * [Glacier Architecture](./docs/7_Storage/7a_S3/Glacier_Architecture.md)
* **Elastic File System (EFS):**
  * [EFS Architecture](./docs/7_Storage/7b_EFS/EFS_Architecture.md)
* **FSx:**
  * [FSx Architecture](./docs/7_Storage/7c_FSx/FSx_Architecture.md)
  * [FSx Lustre](./docs/7_Storage/7c_FSx/FSx_Lustre.md)
* **Storage Gateway:**
  * [File Gateways vs. Volume Gateways vs. Tape Gateway](./docs\7_Storage/7d_Storage_Gateway/File_vs_Volume_vs_Tape_Gateways.md)

--------------------------------

#### Databases

* **Databases Introduction:**
  * [EC2 Self-Managed Databases](./docs/8_Databases/8a_DB_Introduction/EC2_Self-Managed_DB.md)
  * [Database Data Models and Engines](./docs/8_Databases/8a_DB_Introduction/DB_Models_Engines.md)
* **SQL Databases:**
  * [Amazon Relational Database Service (RDS)](./docs/8_Databases/8b_SQL/RDS.md)
  * [Aurora](./docs/8_Databases/8b_SQL/Aurora.md)
  * [Athena](./docs/8_Databases/8b_SQL/Athena.md)
* **NoSQL Databases:**
  * [DynamoDB](./docs/8_Databases/8c_NoSQL/DynamoDB_Architecture.md)
  * [DocumentDB](./docs/8_Databases/8c_NoSQL/DocumentDB.md)
  * [General NoSQL - Neptune & QLDB](./docs/8_Databases/8c_NoSQL/General.md)
* **ElastiCache:**
  * [ElastiCache Architecture](./docs/8_Databases/8d_ElastiCache/ElastiCache_Architecture.md)

--------------------------------

#### Analytics, IoT, and Streaming

* **Elastic Map Reduce:**
  * [Elastic Map Reduce (EMR)](./docs/9_Analytics_IoT_Streaming/9a_EMR/EMR.md)
* **Kinesis:**
  * [Kinesis](./docs/9_Analytics_IoT_Streaming/9b_Kinesis/Kinesis.md)
  * [Kinesis Firehose](./docs/9_Analytics_IoT_Streaming/9b_Kinesis/Kinesis_Firehose.md)
* **Redshift:**
  * [Redshift Overview](./docs/9_Analytics_IoT_Streaming/9c_Redshift/Redshift.md)
* **IoT Platform:**
  * [IoT Overview](./docs/9_Analytics_IoT_Streaming/9d_IoT_Platform/IoT_Architecture.md)
* **QuickSight:**
  * [QuickSight Overview](./docs/9_Analytics_IoT_Streaming/9e_QuickSight/QuickSight.md)
* **Elasticsearch:**
  * [Elasticsearch Overview](./docs/9_Analytics_IoT_Streaming/9f_Elasticsearch/Elasticsearch.md)

--------------------------------

#### Deployment and Operations

* **Monitoring:**
  * [CloudWatch](./docs/10_Deployment_and_Operations/10a_Monitoring/CloudWatch.md)
  * [CloudTrail](./docs/10_Deployment_and_Operations/10a_Monitoring/CloudTrail.md)
* **Systems Manager:**
  * [Systems Manager Overview](./docs/10_Deployment_and_Operations/10b_Systems_Manager/Systems_Manager.md)
  * [Parameters Store](./docs/10_Deployment_and_Operations/10b_Systems_Manager/SSM_Parameters_Store.md)
* **CloudFormation:**
  * [CloudFormation Overview](./docs/10_Deployment_and_Operations/10c_CloudFormation/CloudFormation_Overview.md)
  * [Stack Updates](./docs/10_Deployment_and_Operations/10c_CloudFormation/CloudFormation_Stack_Updates.md)
  * [Template Portability and Reuse](./docs/10_Deployment_and_Operations/10c_CloudFormation/CloudFormation_Template_Portability_Resuse.md)
  * [Stack References and Nested Stacks](./docs/10_Deployment_and_Operations/10c_CloudFormation/CloudFormation_Nested_Stacks.md)
  * [Using CloudFormation for Disaster Recovery](./docs/10_Deployment_and_Operations/10c_CloudFormation/CloudFormation_DR.md)
* **Elastic Beanstalk:**
  * [Elastic Beanstalk Overview](./docs/10_Deployment_and_Operations/10d_Elastic_Beanstalk/Elastic_Beanstalk_Overview.md)
* **OpsWorks:**
  * [OpWorks Overview](./docs/10_Deployment_and_Operations/10e_OpsWorks/OpWorks_Overview.md)
* **AWS Code\***
  * [AWS Code*](./docs/10_Deployment_and_Operations/10f_Code/AWS_Code.md)

--------------------------------

#### Migrations and Hybrid Architectures

* **AWS Data Pipeline:**
  * [Data Pipelines Overview](./docs/11_Migrations_and_Hybrid_Architectures/11a_Data_Pipelines/Data_Pipelines_Essentials.md)
* **AWS Snow\*:**
  * [Snowball and Snowmobile](./docs/11_Migrations_and_Hybrid_Architectures/11b_AWS_Snow/Snowball_Snowmobile.md)

--------------------------------

#### Application Integration

* **Simple Queue Service (SQS):**
  * [SQS Overview](./docs/12_Application_Intergration/12a_SQS/SQS_Overview.md)
* **Simple Notification Service (SNS):**
  * [SNS Overview](./docs/12_Application_Intergration/12b_SNS/SNS_Architecture.md)
* **Amazon MQ:**
  * [Amazon MQ Overview](./docs/12_Application_Intergration/12c_MQ\MQ_Essentials.md)
* **Workflow Orchestration:**
  * [SWS and Step Functions](./docs/12_Application_Intergration/12d_Workflow_Orchestration/SWS.md)

--------------------------------

### Useful Links

Additional links can be found in the content specific links above.

* **Practice Exams:**
  * [Whizlabs](https://www.whizlabs.com/aws-solutions-architect-professional/practice-tests/)
  * [Jon Bonso](https://portal.tutorialsdojo.com/courses/aws-certified-solutions-architect-professional-practice-exams/)
  * [PSI Practice](https://aws.psiexams.com/)

* **AWS Produced Content:**
  * [AWS Certified Solutions Architect – Professional](https://aws.amazon.com/certification/certified-solutions-architect-professional/)
  * [AWS Certified Solutions Architect – Professional (SAP-C01) Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-sa-pro/AWS_Certified_Solutions_Architect_Professional-Exam_Guide_1.2.pdf)
  * [AWS Digital Library](https://www.aws.training/LearningLibrary?&search=&tab=digital_courses)
    * [Exam Readiness: AWS Certified Solutions Architect – Professional](https://www.aws.training/Details/eLearning?id=34737)
    * [AWS Well-Architected](https://www.aws.training/Details/Curriculum?id=42037)
    * [Migrating and Tiering Storage to AWS](https://www.aws.training/Details/eLearning?id=16368)
    * [Deep Dive into Amazon Elastic Block Store (EBS)](https://www.aws.training/Details/eLearning?id=16362)
    * [Deep Dive into Amazon Elastic File System (EFS)](https://www.aws.training/Details/Curriculum?id=25384)
  * **White Papers:**
    * [Securing Data at Rest with Encryption](https://d0.awsstatic.com/whitepapers/aws-securing-data-at-rest-with-encryption.pdf)
    * [Web Application Hosting in the AWS Cloud](https://d0.awsstatic.com/whitepapers/aws-web-hosting-best-practices.pdf?refid=em_)
    * [Migrating AWS Resources to a New Region](http://d0.awsstatic.com/whitepapers/aws-migrate-resources-to-new-region.pdf?refid=70138000001adyu)
    * [AWS Security Best Practices](https://d0.awsstatic.com/whitepapers/Security/AWS_Security_Best_Practices.pdf?refid=em_)
      * [Audio Version](https://soundcloud.com/serverless-guru-871496186/sets/aws-whitepapers)
    * [Implementing Microservices on AWS](https://d1.awsstatic.com/whitepapers/microservices-on-aws.pdf)
    * [Amazon Web Services: Overview of Security Processes](https://d1.awsstatic.com/whitepapers/Security/AWS_Security_Whitepaper.pdf)
    * [Practicing Continuous Integration and Continuous Delivery on AWS](https://d1.awsstatic.com/whitepapers/DevOps/practicing-continuous-integration-continuous-delivery-on-AWS.pdf)
    * [AWS Well-Architected Framework](https://d0.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf)
    * [Building a Scalable and Secure Multi-VPC AWS Network Infrastructure](https://d1.awsstatic.com/whitepapers/building-a-scalable-and-secure-multi-vpc-aws-network-infrastructure.pdf?did=wp_card&trk=wp_card)
  * **FAQs:**
    * [Auto Scaling](https://aws.amazon.com/ec2/faqs/)
    * [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/faqs/)
    * [Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/faqs/)
    * [Lambda](https://aws.amazon.com/lambda/faqs/)
    * [API Gateway](https://aws.amazon.com/api-gateway/faqs/)
    * [DynamoDB](https://aws.amazon.com/dynamodb/faqs/)
    * [CodePipeline](https://aws.amazon.com/codepipeline/faqs/)
    * [CodeCommit](https://aws.amazon.com/codecommit/faqs/)
    * [CodeBuild](https://aws.amazon.com/codebuild/faqs/)
    * [Database Migration Service (DMS)](https://aws.amazon.com/dms/faqs/)
    * [Organizations](https://aws.amazon.com/organizations/faqs/)
    * [Server Migration Service](https://aws.amazon.com/server-migration-service/faqs/)
    * [Serverless Application Model](https://aws.amazon.com/serverless/sam/faqs/)
    * [EC2 Systems Manager](https://aws.amazon.com/systems-manager/faq/)
    * [Service Catalog](https://aws.amazon.com/servicecatalog/faqs/)
    * [Direct Connect](https://aws.amazon.com/directconnect/faqs/)
    * [Transit Gateway](https://aws.amazon.com/transit-gateway/faqs/)
    * [Key Management Service (KMS)](https://aws.amazon.com/kms/faqs/)

* **Adrian Cantril:**
  * [Solutions Architect - Professional Course](https://learn.cantrill.io/p/aws-certified-solutions-architect-professional)

* **Udemy:**
  * [Stephane Maarek's Course](https://www.udemy.com/course/aws-solutions-architect-professional/)

* **Linux Academy:**
  * [The Orion Papers Pro](https://interactive.linuxacademy.com/diagrams/OrionPapersPro.html)

* **Pluralsight:**
  * [AWS Certified Solutions Architect - Professional Path](https://app.pluralsight.com/paths/certificate/aws-certified-solutions-architect-professional)

* **Tutorial Dojo:**
  * [AWS Cheat Sheets](https://tutorialsdojo.com/aws-cheat-sheets/)

* **Other:**
  * [AWS In Plain English](https://expeditedsecurity.com/aws-in-plain-english/)
  * [AWS Certification Reddit](https://www.reddit.com/r/AWSCertifications/)

--------------------------------

## Planned Approach

* [x] **Watch Linux Academy Course Through**
* [ ] **Work Through Adrian Cantrill's SA Pro Course (If Available)**
* [ ] **Watch AWS Digital Library:**
  * [ ] Exam Readiness: AWS Certified Solutions Architect – Professional
  * [ ] AWS Well-Architected
  * [ ] Migrating and Tiering Storage to AWS
  * [ ] Deep Dive into Amazon Elastic Block Store (EBS)
  * [ ] Deep Dive into Amazon Elastic File System (EFS)
* [ ] **Read FAQs:**
  * [ ] Auto Scaling
  * [ ] Elastic Load Balancing
  * [ ] Elastic Beanstalk
  * [ ] Lambda
  * [ ] API Gateway
  * [ ] DynamoDB
  * [ ] CodePipeline
  * [ ] CodeCommit
  * [ ] CodeBuild
  * [ ] Database Migration Service (DMS)
  * [ ] Organizations
  * [ ] Server Migration Service
  * [ ] Serverless Application Model
  * [ ] EC2 Systems Manager
  * [ ] Service Catalog
  * [ ] Direct Connect
  * [ ] Transit Gateway
  * [ ] Key Management Service (KMS)
* [ ] **Take Practice Exams:**
  * [ ] 1 Bonso
  * [ ] 1 Whizlab
* [ ] **Read Whitepapers:**
  * [ ] Securing Data at Rest with Encryption
  * [ ] Web Application Hosting in the AWS Cloud
  * [ ] Migrating AWS Resources to a New Region
  * [ ] AWS Security Best Practices
  * [ ] Implementing Microservices on AWS
  * [ ] Amazon Web Services: Overview of Security Processes
  * [ ] Practicing Continuous Integration and Continuous Delivery on AWS
  * [ ] AWS Well-Architected Framework
  * [ ] Building a Scalable and Secure Multi-VPC AWS Network Infrastructure
* [ ] **Watch Stephane Maarek's Udemy Course**
* [ ] **Take Practice Exams:**
  * [ ] Bonso
  * [ ] Whizlab
  * [ ] PSI
* [ ] **Review**
* [ ] **Schedule Exam**
