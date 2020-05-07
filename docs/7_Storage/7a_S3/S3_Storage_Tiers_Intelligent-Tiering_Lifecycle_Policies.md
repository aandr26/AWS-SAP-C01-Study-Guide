# S3 Storage Tiers, Intelligent-Tiering, and Lifecycle Policies

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Amazon S3 Storage Classes](https://aws.amazon.com/s3/storage-classes/)

* **Exam Tips:**
  * Every object must have an associated storage class (tier).
  * All share 11 nine durability.
  * **S3 Storage Tiers:**
    * **S3 Standard:**
      * General objects.
      * This is the default storage class.
      * A target of 99.99% availability over the year (The availability SLA is   99.9%).
      * Replication to at least 3 AZs.
      * First-byte latency of a millisecond(s).
    * **Infrequent Access S3-IA:**
      * For infrequent access to important objects that require quick retrival.
      * A target of 99.9% availability over the year (The availability SLA is   99%).
      * Replication to at least 3 AZs.
      * Less expensive than Standard.
      * Minimum storage charge of 30 days per object, plus a minimun storage   charge of 128 KB, and a retrival fee.
      * First-byte latency of a millisecond(s).
    * **S3 One Zone-IA:**
      * Used for non-critical, reproducible.
      * A target of 99.5% availability over the year (The availability SLA is   99%).
      * _Only 1 AZ replication_
      * Minimum storage charge of 30 days per object, plus a minimun storage   charge of 128 KB, and a retrival fee.
      * Less expensive than Standard and S3-IA
    * **S3 Intelligent-Tiering:**
      * Designed for unknown or unpredictable access patterns.
      * Moves ovjects between two tiers:
        * One for frequent access.
        * One for infrequent access.
  * **Glacier Storage Tiers:**
    * **Glacier:**
      * Technically Glacier is a seperate product.
      * Used for long-term archival storage - Don't use for backups!
      * Cheapest storage class.
      * Replication to at least 3 AZs.
      * A minimum of 90 days charge per object, 40 KB minimun storage charge, and a retrival fee.
    * **Glacier Deep Archive:**
      * Used for long-term archival storage.
        * Think of as an ideal alternative to tape backups.
      * Even cheaper than Glacier storage, but longer to retrieve.
      * Replication to at least 3 AZs.
      * A minimum of 180 days charge per object, 40 KB minimun storage charge, and a retrival fee.
  * **Lifecycle Policies:**
    * Rules are at a bucket level.
    * Can configure move between tiers or expire the object..
    * Can be used to move objects into Glacier for archiving.
    * Some movement is one way (cannot move from Glacier back to Standard.)
  