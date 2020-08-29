# RDS Multi-AZ

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Synchronous replication = Multi-AZ.
    * Can only occur in one region between two AZs.
    * Only really used for availability, not performance!
  * Multi-AZ not available with the free-tier.
    * Extra cost for standby replica.
  * Standby can't be directly used.
  * 60-120 seconds failover.
  * Same region only (other AZs in the VPC).
  * Backups taken from standby (removes performance impact).
  * AZ outage, primary failure, manual failover, instance type change and software patching.
