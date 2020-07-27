# ElastiCache Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [ElastiCache Use Cases](https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/elasticache-use-cases.html)
  * [Choosing between Redis and Memcached](https://aws.amazon.com/elasticache/redis-vs-memcached/)
  * [Fault Tolerance in ElastiCache](https://aws.amazon.com/premiumsupport/knowledge-center/fault-tolerance-elasticache/)
  * [Tutorials Dojo ElastiCache Cheat Sheet](https://tutorialsdojo.com/amazon-elasticache/)

* **Exam Tips:**
  * Supports any RDS DB or even no DB at all is required.
  * Be aware of scenarios where it is need:
    * Used to improve database performance by caching query results.
    * Used where read heavy workloads with low latency requirements.
    * Reduces database workloads, meaning savings.
    * Application needs to know to use caching. - Application changes.
  * Understand the differences between Redis and Memcached:
    * Advanced data structures beyond key value stores, you have to use Redis.
    * Vertical scaling = Memcached
    * High Availability = Redis
    * Data Durability:
      * Redis data is not persistent by default, but you can enable the Append-Only File (AOF). This allows the Redis node to write all of the commands that modify the cache data to an append-only file.
      * In the case a Redis node is rebooted, the AOF allows the Redis node to have a warm cache with the data intact.
      * Disabled by default, enabled by assigning a parameter group with ```appendonly``` set to yes.
      * You can use ```appendfsync``` to determine how often the AOF file is written to.
