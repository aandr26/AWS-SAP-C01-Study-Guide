# Advanced VPC Structure

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * **AZs:**
    * You'll need to know how many subnets are required in a VPC.
      * Cost effective, cost effective, cost effective!
      * How to calculate required AZ
        * Most questions ask about designing a solution that can tolerate 1 AZ  failure, which is called the buffer AZ.
        * AZs in region (6) minus buffer AZs (1) = 5 (Nominal AZs)
        * Min app requirements? 5 nominal instances in this example
        * Nominal instances / nominal AZs (5/5) = Optimal 1 per AZ
      * Pay attention to min AZ vs cost effective.
  * **Subnets and Tiers:**
    * 1 tier in 3 AZ = 3 subnet design (one subnet one AZ)
    * If DB cannot be in the same subnet as the app servers, than they will be in their own subnets in their own tier.
    * 2 tier in 3 AZ = 6 subnet design (one subnet one AZ)
    * Ignore HA to start with.
    * How many subnets does your app need?
    * Public & private addressing, and security can be controlled with one subnet.
    * Different routing = multiple subnets.
    * Internet-facing ALBs can communicate with private instances.
      * Needs to run from public subnets.
    * N of app subnets * AZs = number of subnets needed.
