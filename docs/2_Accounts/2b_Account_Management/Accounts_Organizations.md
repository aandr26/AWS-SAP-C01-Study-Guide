# AWS Accounts and AWS Organizations

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Using Consolidated Billing](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/useconsolidatedbilling-discounts.html)
  * [Organizations Docs](https://docs.aws.amazon.com/organizations/?id=docs_gateway)
  * [AWS Service Limits](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)
  * [Service Endpoints and Quotas](https://docs.aws.amazon.com/general/latest/gr/aws-general.pdf#aws-service-information)
  * [IAM Limits](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-limits.html)
  * [AWS re:Invent 2019: Architecting security & governance across your landing zone (SEC325)](https://youtu.be/zVJnenaD3U8)

* **Notes:**
  * Used to be known as the '_payer_' account, now known as the '_master_' account.
  * Accounts joined to the organization are known as member accounts.
  * IAM Policy management.
  * Consolidated billing:
    * May gain you volume discounts, thus reducing your bill.
  * OUs = Organizational Unit.
  * Treat master account as a billing and user store.

## Service Control Policies

* **Notes:**

* SCP inherit downwards, but they _do not_ affect the master account.

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
