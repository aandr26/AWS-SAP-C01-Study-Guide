# Object Encryption

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * **Server-side Encryption (SSE):**
    * **Customer-Provided Keys (SSE-C):**
      * You are completly responsible for managing these keys.
    * **S3-Managed Keys (SSE-S3):**
      * AWS managed key.
      * Master key is regulary rotated.
      * The default encryption key.
    * **KMS-Managed Keys (SSE-KMS):**
      * Allows a role split.
      * Can give separate set of permissions between KMS and S3
      * Allows for some more control over the master key.
  * You are not encrypting a bucket, you are encrypting the objects!
  * The default encryption setting defines what default encryption policy will be used if an encryption type is not defined.
    * Can create bucket policy that enforces using a specific encryption when uploading objects.
