# Database Data Models and Engines

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Graph Databases for Beginners: ACID vs. BASE Explained](https://neo4j.com/blog/acid-vs-base-consistency-models-explained/)
  * [A Comparison of NoSQL Database Management Systems and Models](https://www.digitalocean.com/community/tutorials/a-comparison-of-nosql-database-management-systems-and-models)

* **Exam Tips:**
  * **Relational Database:**
    * RDBMS used for data that needs to be managed with formal and fixed relationships.
    * Doesn't scale well.
    * Not suitable for dynamic data.
    * Favors data that is defined upfront and fixed.
    * Uses ACID (Atomicity, Consistency, Isolation, Durability)
      * The tradeoff is in performance - it is slower.
    * Best for transactional, highly structured.
  * **NoSQL:**
    * **Key Value:**
      * No structure.
        * DynamoDB
        * Redis
      * Super fast queries and great scalability.
      * Great for WebApps
    * **Document DB:**
      * Not concerned as much with relationships between the data.
      * Great for nested information.
      * Think MongoDB
    * **Column Based DB:**
      * Really fast queries.
      * Data warehouses
      * Analytics
      * Reporting
      * Think Redshift
      * Not used for transactions!
    * **Graph DB:**
      * Designed for dynamic relationships
      * Ideal for data related to 'humans'
        * Social media
        * Dynamic community data
