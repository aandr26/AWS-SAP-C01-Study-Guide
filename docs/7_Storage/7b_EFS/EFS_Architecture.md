# EFS Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Amazon EFS Performance](https://docs.aws.amazon.com/efs/latest/ug/performance.html)
  * [Amazon EFS Performance Tips](https://docs.aws.amazon.com/efs/latest/ug/performance-tips.html)
  * [Using the amazon-efs-utils Tools](https://docs.aws.amazon.com/efs/latest/ug/using-amazon-efs-utils.html)
  * [Tutorials Dojo EFS Cheat Sheet](https://tutorialsdojo.com/amazon-efs/)

* **Exam Tips:**
  * Questions about shared file systems, mountable - specifically Linux?
    * EFS
  * By default it is private, via mount targets inside a VPC.
  * Access via Lambda.
  * Highly scalable, highly available.
  * Can POSIX permissions.
  * Supports encryption at rest.
  * Billed for size used.
  * **Performance Mode:**
    * Cannot change after creation!
    * General Purpose:
      * Webservers
      * Content hosting
      * Homefolders
    * **Max I/O:**
      * Higher throughput in IOPs
        * Suitable for parallel workloads.
    * Replicated across multiple AZs.
    * **Use cases:**
      * Big data/analytics
      * Media workloads
      * CM and websharing
      * Home directories
      * Shared log storage (depending on application)
    * **Anti-Patterns:**
      * For single machine.
      * Object storage.
      * Temporary storage.
