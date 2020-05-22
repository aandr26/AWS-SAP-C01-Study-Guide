# AWS Accounts and AWS Organizations

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Using Consolidated Billing](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/useconsolidatedbilling-discounts.html)
  * [Organizations Docs](https://docs.aws.amazon.com/organizations/?id=docs_gateway)
  * [AWS Service Limits](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)
  * [Service Endpoints and Quotas](https://docs.aws.amazon.com/general/latest/gr/aws-general.pdf#aws-service-information)
  * [IAM Limits](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-limits.html)
  * [RI Sharing in Organizations](https://aws.amazon.com/blogs/publicsector/controlling-how-your-aws-credits-and-ri-discounts-are-shared-across-your-organization/)

* **Exam Tips:**
  * Used to be known as the '_payer_' account, now known as the '_master_' account.
  * Accounts joined to the organization are known as member accounts.
  * IAM Policy management.
  * **Consolidated billing:**
    * May gain you volume discounts, thus reducing your bill.
  * **RI Credit Sharing:**
    * You can enable Reserved Instance sharing in the member accounts and then purchase Reserved Instances in the master account.
      * EC2
      * RDS
      * Redshift
    * You can disable credit sharing globally in a master account- it is enabled by default.
    * Each member account can disable or enable RI sharing. This is generally done on a use case basis, as in when you want to keep certian business units seperate.
    * The billing console in the master account allows you to manage which member accounts do or do not take part in RI sharing. Again, the default is to share RI.
  * OUs = Organizational Unit.
  * Treat master account as a billing and user store.

## Service Control Policies

* **Exam Tips:**
  * They do not provide actual permissions, they only allow or deny actions.
    * Default policy is to allow all actions on all resources.
    * Need explicit allows and explicit deny.
      * Explicit deny always overrides an allow.
      * Anything else not defined gets an implicit deny.
  * SCP inherit downwards, but they do not affect the master account.
    * They do not affect the master account in **_anyway!_**

## Account Limits

* **Exam Tips:**
  * Try to understand limits that will affect any architecture designs:
    * [IAM](https://docs.aws.amazon.com/general/latest/gr/iam-service.html)
    * [EBS Volumes](https://docs.aws.amazon.com/general/latest/gr/ebs-service.html)
    * [S3 Buckets](https://docs.aws.amazon.com/general/latest/gr/s3.html)
    * [Using Service Quotas Request Templates](https://docs.aws.amazon.com/servicequotas/latest/userguide/organization-templates.html)
  * You can request service quotas for most services.
    * Some services do not support quotas.
  * Perferred method is to use the service quotas console.
    * Can use the cli to request more.
  * You can configure CloudWatch alarms for service qoutas limits.

## AWS Support Tiers

* **Exam Tips:**
  * Difference between enhanced techical support.
  * Architectual guidance.
    * Business and Enterprise
  * Programmatic case management.
    * Business and Enterprise
  * Proactive programs.
    * Business (extra cost) and Enterprise.
  * Technical account management.
    * Enterprise.
