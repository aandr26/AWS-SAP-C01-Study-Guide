# FSx for Lustre

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Lustre FSx Aggregate Performance](https://docs.aws.amazon.com/fsx/latest/LustreGuide/performance.html#fsx-aggregate-perf)

* **Exam Tips:**
  * Supports POSIX
  * HPC, ML, Big Data = Lustre
  * Metadata stored on Metadata Targets (MST)
  * Objects are stored on object storage targets (OSTs) (1.17TiB)
  * Baseline performance based on size
  * Size - min 1.2TiB then increments of 2.4TiB
  * For Scratch - Base 200 MB/s per TiB of storage
  * Persistent offers of 50 MB/s, 100 MB/s, and 200 MB/s per TIB of storage
  * Burst up to 1300 MB/s per TiB (Credit System).
  * **Deployment Types:**
    * Scratch:
      * Pure performance
      * Short term of temp workloads
      * No HA
      * No Replication
    * Persistent:
      * Has replication with one AZ only
      * Backup to S3 (Manual or automatic 0-35 day retention.)
