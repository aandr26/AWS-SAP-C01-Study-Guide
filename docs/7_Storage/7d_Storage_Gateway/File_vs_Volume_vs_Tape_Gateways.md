# File Gateways vs. Volume Gateways vs. Tape Gateway

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Using the AWS Storage Gateway Hardware Appliance](https://docs.aws.amazon.com/storagegateway/latest/userguide/HardwareAppliance.html)
  * [How AWS Storage Gateway Works (Architecture)](https://docs.aws.amazon.com/storagegateway/latest/userguide/StorageGatewayConcepts.html)
  * [Tutorials DOJO Storage Gateway Cheat Sheets](https://tutorialsdojo.com/aws-storage-gateway/)

* **Exam Tips:**
  * **Volume Gateway:**
    * **Stored Volumes:**
      * Raw, block storage via iSCSI.
      * Stored locally.
      * Great for full disk **backups** of.
      * Assist with disaster recovery.
      * Does not improve datacenter capacity.
        * Main copy of data is stored on the gateway.
    * **Cached Volumes:**
      * Raw, block storage via iSCSI.
      * Primary location is now S3, with frequently access data cached locally.
      * AWS managed S3, cannot browse to the bucket.
      * Data center extension.
  * **Tape Gateway:**
    * VTL
  * **File Gateway:**
    * Bridges on-premises file storage and S3.
    * Mount points available via NFS or SMB.
    * Map directly on an S3 bucket.
    * Files stored into a mount point, are visible as objects in an S3 Bucket.
    * Read and write caching ensure LAN-like performance.
    * Primary data stored in S3.
    * Up to 10 shares.
  * Migrate file storage data exam questions?
    * File Gateway.
