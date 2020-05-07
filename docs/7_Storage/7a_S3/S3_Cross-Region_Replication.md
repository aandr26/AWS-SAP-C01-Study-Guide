# Cross-Region Replication

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Default is to replicated un-encrypted.
    * Supports SS3-S3 by default and SSE-KMS.
    * Does not support customer created keys.
  * Storage class and object ownerships are replicated, but not lifecycle policies.
  * Changes made to an object in the replicated region are not replicated back to the source bucket. It is one way!
