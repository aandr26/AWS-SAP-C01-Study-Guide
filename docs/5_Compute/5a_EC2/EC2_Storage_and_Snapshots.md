# EC2 Storage and Snapshots

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Instance storage](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html)
  * [EC2 and EBS Performance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSPerformance.html)
  * [EBS Volume Types and Performance Information](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html)

* **Exam Tips:**
  * **Ephemeral Storage (Instance Store Volumes):**
    * Limitations
    * Risks
    * Performance Characteristics.
  * Know the ideal patterns and anti-patterns for ephemeral storage:
    * Ideal:
      * Temporary storage
      * High I/O & Throughput
    * Anti-Patterns:
      * Shared storage
      * Persistence
      * Durability/Resilience
      * Elasticity
    * Maximum performance possible? Use Instance Store Volumes.
  * **EBS:**
    * Supports a meximum per instance throughput of 1,750 MiB/s and 80,000 IOPS.
    * Be aware of what storage you might use given a situation.
    * SSD Based:
      * General Purpose (gp2)
      * Provisioned IOPS SSD (io1)
        * IOPS can scale seperately of the volume size.
    * HDD:
      * Throughput Optimized (st1)
      * Cold HDD (sc1)
    * Know the ideal patterns and anti-patterns for EBS storage:
      * Ideal
        * Persistence
        * Durability
        * Elasticity
        * Provisioned performance
      * Anti-Patterns:
        * Temporary storage
        * Static Content Distribution
        * Shared Access
        * High Durability (99.5 - 99.9+)
    * Does not provide storage sharing, use EFS instead.
    * **Snapshots:**
