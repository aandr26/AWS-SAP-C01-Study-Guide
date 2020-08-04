# Amazon Aurora Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Deep Dive on Amazon Aurora with MySQL Compatibility](https://www.youtube.com/watch?v=U42mC_iKSBg)
  * [What's New in Amazon Aurora](https://www.youtube.com/watch?v=2WG01wJIGSQ)

* **Exam Tips:**
  * Custom designed by AWS:
    * MySQL and PostgreSQL compatibility
    * 5x performance of MySQL
    * 3x performance of PostgreSQL
  * No master slave architecture.
  * Reader endpoints maps to any replica instances.
  * Aurora Cluster Storage is replicated 6+ times across 3 availability zones at the storage level. 
    * Only region failure would significantly impact service.
  * Data is replicated at the storage level automatically
  * Individual endpoints can be reached using their endpoint ids.
  * Storage:
    * Up to 64 TB
    * Pay for what you use.
  * **Aurora Global Database:**
    * Achieves high throughput
    * Recovers quickly in the case of a regional failure.
    * Replication between local and remote region.
  * **Aurora Serverless:**
    * Pay for what you use:
      * There is a minimum capacity unit and a maximum.
