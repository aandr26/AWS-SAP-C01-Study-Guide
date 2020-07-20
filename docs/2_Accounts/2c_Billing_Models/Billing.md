# Resource Billing Modes: On-Demand, Reserved, and Spot

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [AWS Openguide Billing and Cost Management](https://github.com/open-guides/og-aws#billing-and-cost-management)

* **Exam Tips:**
  * **1. On-Demand**
    * Standard startup priority.
    * Default
    * Pay for what you consume.
    * Per second billing.
    * no capcity reservation
    * no discount.
    * Use:
      * Short term workloads
      * Unknown workloads
      * Apps which cannot be interrupted
  * **2. Reserved**
    * 12 or 36-month term
      * All Upfront (best cost advantages), Partial Upfront, and No Upfront.
    * Can be used for:
      * EC2 Instances
      * RDS
      * DynamoDB
      * Other services
    * Can reserve capacity providing high-priority startup.
  * **3. Spot**
    * Can be shutoff without notice.
    * Lowest startup priority.
