# Amazon Aurora Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [AWS re:Invent 2018: Deep Dive on Amazon Aurora with MySQL Compatibility](https://www.youtube.com/watch?v=U42mC_iKSBg)

* **Exam Tips:**
  * Custom designed by AWS:
    * MySQL and PostgreSQL compatability
    * 5x performance of MySQL
    * 3x performance of PostgreSQL
  * No master slave architecture.
  * Reader endpoints maps to any replica instances.
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
