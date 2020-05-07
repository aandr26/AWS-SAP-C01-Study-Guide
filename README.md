# AWS Certified Solutions Architect - Professional Exam Guide

## About

This guide serves to help the user pass the AWS Certified Solutions Archictect - Professional exam.

It generally follows the Linux Academy [AWS Certified Solutions Architect - Professional](https://linuxacademy.com/course/aws-certified-solutions-architect-professional-2018/) course, but includes some additional content that will supplement.

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

* **Advanced Identity in AWS:**
  * [IAM Permission Boundaries](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/IAM_Permission_Boundaries.md)
  * [Identity Federation](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/Identity_Federation.md)
  * [Policy Evaluation Logic](./docs/2_Accounts/2d_Advanced_Identity_in_AWS/Policy_Evaluation_Logic.md)

--------------------------------

#### Networking

* **Essentials:**
  * [VPC Basics](./docs/3_Networking/3a_VPC_Essentials/VPC_Basics.md)
  * [Resource Access Manager](./docs/3_Networking/3a_VPC_Essentials/Resource_Access_Manager.md)
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

--------------------------------

#### Security

* **Account and Service Security:**
  * [Key Management Service (KMS)](./docs/4_Security/4a_Account_Service_Security/Key_Management_Service_KMS.md)
  * [CloudHSM](./docs/4_Security/4a_Account_Service_Security/CloudHSM.md)
  * [Certificate Manager (ACM)](./docs/4_Security/4a_Account_Service_Security/Certificate_Manager_ACM.md)
  * [Directory Service](./docs/4_Security/4a_Account_Service_Security/Directory_Service.md)

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
  * [ECS Architecture](./docs/5_Compute/5b_Containers/ECS_Archictecture.md)
  * [ECS Security](./docs/5_Compute/5b_Containers/ECS_Security.md)
* **Serverless:**
  * [Serverless and Event-Driven Architectures](./docs/5_Compute/5c_Serverless/Serverless_Event-Driven_Archictectures.md)
  * [Lambda Layers](./docs/5_Compute/5c_Serverless/Lambda_Layers.md)
  * [API Gateway](./docs/5_Compute/5c_Serverless/API_Gateway.md)

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
  * [Versioning and Locking](./docs/7_Storage/7a_S3/Versioning_and_Locking.md)

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
    * [Web Appilcation Hosting in the AWS Cloud](https://d0.awsstatic.com/whitepapers/aws-web-hosting-best-practices.pdf?refid=em_)
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
    * [CodePipline](https://aws.amazon.com/codepipeline/faqs/)
    * [CodeCommit](https://aws.amazon.com/codecommit/faqs/)
    * [CodeBuild](https://aws.amazon.com/codebuild/faqs/)
    * [Database Migration Service (DMS)](https://aws.amazon.com/dms/faqs/)
    * [Oraganizations](https://aws.amazon.com/organizations/faqs/)
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

  * **Labs that Linux Academy Recommends**
    * [Recap: Provisioning an EC2 Instance](https://linuxacademy.com/cp/livelabs/view/id/161/module/119)
    * [EC2 Backup Solutions with AMIs and Snapshots](https://linuxacademy.com/cp/livelabs/view/id/188/module/119)
    * [Accessing an Instance's User Data and Metadata](https://linuxacademy.com/cp/livelabs/view/id/162/module/119)
    * [Setting up an ELB and Auto Scaling Group](https://linuxacademy.com/cp/livelabs/view/id/165/module/119)
    * [Building a More Secure Application with a Bastion Host and NAT Gateway](https://linuxacademy.com/cp/livelabs/view/id/163/module/119)
    * [Using S3 for Static Web Hosting](https://linuxacademy.com/cp/livelabs/view/id/173/module/119)
    * [Configuring Backup and Archiving Solution in S3](https://linuxacademy.com/cp/livelabs/view/id/172/module/119)
    * [Configuring Route 53 DNS Records Sets](https://linuxacademy.com/cp/livelabs/view/id/166/module/119)
    * [Configuring a CloudFront Distribution](https://linuxacademy.com/cp/livelabs/view/id/167/module/119)
    * [VPC Peering](https://linuxacademy.com/cp/livelabs/view/id/182/module/119)
    * [RDS Lab](https://linuxacademy.com/cp/livelabs/view/id/175/module/119)
    * [Create and Use an SNS Topic with S3 Events](https://linuxacademy.com/cp/livelabs/view/id/174/module/119)
    * [CloudWatch Sandbox](https://linuxacademy.com/cp/livelabs/view/id/178/module/119)
    * [CloudTrail Sandbox](https://linuxacademy.com/cp/livelabs/view/id/179/module/119)
    * [CloudFormation Lab](https://linuxacademy.com/cp/livelabs/view/id/180/module/119)
    * [Elastic Beanstalk Lab](https://linuxacademy.com/cp/livelabs/view/id/181/module/119)

* **Pluralsight:**
  * [AWS Certified Solutions Architect - Professional Path](https://app.pluralsight.com/paths/certificate/aws-certified-solutions-architect-professional)

* **Tutorial Dojo:**
  * [AWS Cheat Sheets](https://tutorialsdojo.com/aws-cheat-sheets/)

* **Other:**
  * [AWS In Plain English](https://expeditedsecurity.com/aws-in-plain-english/)
  * [AWS Certification Reddit](https://www.reddit.com/r/AWSCertifications/)

--------------------------------

## Planned Approach

* [ ] **Watch Linux Academy Course Through**
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
  * [ ] CodePipline
  * [ ] CodeCommit
  * [ ] CodeBuild
  * [ ] Database Migration Service (DMS)
  * [ ] Oraganizations
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
  * [ ] Web Appilcation Hosting in the AWS Cloud
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
