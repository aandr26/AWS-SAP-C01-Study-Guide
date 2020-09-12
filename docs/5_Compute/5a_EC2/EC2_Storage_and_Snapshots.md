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
    * Supports a maximums per instance throughput of 1,750 MiB/s and 80,000 IOPS.
    * Be aware of what storage you might use given a situation.
    * SSD Based:
      * General Purpose (gp2)
      * Provisioned IOPS SSD (io1)
        * IOPS can scale separately of the volume size.
    * HDD:
      * Cannot be used as a boot volume.
      * Throughput Optimized (st1)
        * Frequently accessed.
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
    * **Question Tips:**
      * Cheap = ST1 or SC1
      * Throughput / streaming = ST1
      * Boot = NOT ST1 or SC1
      * GP2 = up to 16,000 IOPS
      * IO1/2 = up to 64,000 IOPS
      * RAID0 + EBS = up to 160,000 IOPS
      * More than 160,000 IOPS = Instance Store
