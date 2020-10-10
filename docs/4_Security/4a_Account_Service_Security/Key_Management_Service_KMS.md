# AWS Key Management Service (KMS)

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [FIPS 140-2](https://en.wikipedia.org/wiki/FIPS_140-2)
  * [Importing Keys](https://docs.aws.amazon.com/kms/latest/developerguide/importing-keys.html)
  * [Enveloping](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#enveloping)
  * [Protecting Encrypted Data Integrity](https://aws.amazon.com/blogs/security/how-to-protect-the-integrity-of-your-encrypted-data-by-using-aws-key-management-service-and-encryptioncontext/)
  * [Grants](https://docs.aws.amazon.com/kms/latest/developerguide/grants.html)
  * [Compliance](https://aws.amazon.com/kms/details/#compliance)
  * **Not Required Knowledge:**
    * [AWS re:invent 2017: Best Practices for Implementing AWS Key Management Service (SID330)](https://www.youtube.com/watch?v=X1eZjXQ55ec)

* **Notes:**
  * Generates CMK (Customer Master Keys)
    * Once generated, able to encrypt or decrypt data up to 4KB in size.
    * Logically the CMK doesn't leave the service, KMS, or the region.

* **Exam Tips:**
  * Role separation:
    * Don't have to give S3 users access to decrypt.
    * FIPS 140-2 compliant service? Use KMS as it supports up to level 2.
    * Can only be managed by AWS APIs.
    * CMKs can only be used for up to 4KB of data.
    * CMKs support rotation.
    * CMKs are more configurable.
