# Amazon Aurora Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Deep Dive on Amazon Aurora with MySQL Compatibility](https://www.youtube.com/watch?v=U42mC_iKSBg)
  * [What's New in Amazon Aurora](https://www.youtube.com/watch?v=2WG01wJIGSQ)

* **Exam Tips:**
  * Uses a cluster
  * Backups:
    * Backtrack:
      * Used to allow in-place rewinds to a previous point in time.
    * Restores create a new cluster.
    * Fast clones make a new database much faster than copying all the data - copy-on-write.
  * A single primary instance + 0 or more replicas
  * Custom designed by AWS:
    * MySQL and PostgreSQL compatibility
    * 5x performance of MySQL
    * 3x performance of PostgreSQL
  * No master slave architecture.
  * Reader endpoints maps to any replica instances.
  * Aurora Cluster Storage is replicated 6+ times across 3 availability zones at the storage level.
    * Only region failure would significantly impact service.
  * Cluster level storage:
    * Data is replicated at the storage level automatically.
    * 6 replicas across AZs
    * Up to 64 TB
    * Pay for what you use.
  * Individual endpoints can be reached using their endpoint ids.
  * **Aurora Global Database:**
    * Achieves high throughput
    * Recovers quickly in the case of a regional failure.
    * Replication between local and remote region.
  * **Aurora Serverless:**
    * Pay for what you use:
      * There is a minimum capacity unit and a maximum.
    * Use cases:
      * Infrequently used applications.
      * New applications.
      * Variable workloads.
      * Unpredictable workloads.
      * Development and test databases.
      * Multi-tenant applications.
