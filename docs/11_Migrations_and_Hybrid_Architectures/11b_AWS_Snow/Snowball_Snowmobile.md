# Migrating Data to AWS with Snowball and Snowmobile

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [What Is an AWS Snowball Device?](https://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)
  * [How AWS Snowball Works with the Snowball Edge](https://docs.aws.amazon.com/snowball/latest/developer-guide/how-it-works.html)
  * [Best Practices for the AWS Snowball Edge Device](https://docs.aws.amazon.com/snowball/latest/developer-guide/BestPractices.html)
  * [AWS Snowball Device Differences](https://docs.aws.amazon.com/snowball/latest/developer-guide/device-differences.html)

* **Exam Tips:**
  * **Snowball:**
    * 50 TB or 80 TB per device.
    * Use when transferring more than 10 TB
    * Can chain together to get more capacity.
    * Faster than internet/Direct Connect/VPN
  * **Snowball Edge:**
    * Up to 100 TB per device - Storage Optimized
    * Provide local computer services, running processes at the edge:
      * Lambda functions
      * EC2 Instances
    * **Three versions:**
      * Storage Optimized - 100 TB with 80 TB usable
      * Compute Optimized - Super fast nvme SSD
      * Compute Optimized with GPU - Analytics
  * **Snowmobile:**
    * 100 PB per Snowmobile, can be used in parallel.
    * Mobile data center
    * Data center migrations
    * Use when transferring more than 10 PB.
      * Less than 10 PB use one or more Snowball/Snowball Edge.
      * Multiple locations - Same as above.
