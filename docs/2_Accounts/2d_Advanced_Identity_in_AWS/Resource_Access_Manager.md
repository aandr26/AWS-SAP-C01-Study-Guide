# AWS Resource Access Manager

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Enable RAM](https://console.aws.amazon.com/ram/home#Setting)
  * [Working with AZ IDs](https://docs.aws.amazon.com/ram/latest/userguide/working-with-az-ids.html)
  * [What is AWS RAM?](https://docs.aws.amazon.com/ram/latest/userguide/what-is.html)
  * [VPC Sharing](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-sharing.html)

* **Notes:**
  * Owners and participants

* **Exam Tips:**
  * Be familier with AZ ids vs name.
  * Subnet sharing can only happen with other accounts in your organization.
  * VPC owners can create and manage the VPC and subnets and share to the participants.
    * Participants can provision services into the shared subnets, read, and reference network objects but not modify or delete the VPC and subnets.
  * Whatever the parcipants create in the shared resources belongs to them.
  * The owner cannot delete or modify resources created by participant VPCs.
