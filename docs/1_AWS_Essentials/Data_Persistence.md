# Data Persistence

* [Return to table of contents](../../README.md)

* **Exam Tips:**
  * **Ephemeral**
    * Data this is local to a resource (usually) and lost when the resource is powered off.
      * Instance Store Volume
        * Attached to host in an AZ, failure of either host or AZ means failure of the volume.
      * Amazon ElastiCache
    * Very high throughput.
    * Data is *lost* when the resource is powered down.
    * Data does survive a reboot, but if an instance is terminated or the disk itself fails, the data is lost.
  * **Persistent**
    * Data that is durable and able to survive power events such as start, stop, and restart.
      * Amazon EBS (Elastic Block Store)
        * Replicates within an AZ.
        * Failure of AZ means failure of a volume.
        * Can store snapshots in S3 which is regionally resilient, and then copy the snapshots to S3 buckets in other regions.
      * Amazon EFS (Elastic File Store)
        * Replicated across multiple AZs- By default regionally resilient.
        * Failure of the region means failure of the filesystem.
    * Comes at an extra cost.
    * Not default.
    * Good for things such as databases.
  * **Transient**
    * Datastores that exist with the intention that the data injected is temporary.
      * SQS
    * Not used for permanent storage.
    * Used as intermediaries between services.
