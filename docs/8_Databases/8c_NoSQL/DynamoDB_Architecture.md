# DynamoDB Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [General Guidelines for Secondary Indexes in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-indexes-general.html)
  * [Read Consistency](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadConsistency.html)
  * [Concepts](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.concepts.html)
  * [Time To Live: How It Works](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/howitworks-ttl.html)
  * [Using IAM Policy Conditions for Fine-Grained Access Control](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/specifying-conditions.html)
  * [Amazon DynamoDB Deep Dive: Advanced Design Patterns for DynamoDB](https://www.youtube.com/watch?v=HaEPXoXVf2k)

* **Exam Tips:**
  * NoSQL = preference DynamoDB in the exam.
  * Key/Value preference DynamoDB in the exam.
  * If question references relational data or mentions SQL, generally not DynamoDB.
  * Bill based RCU, WCU, storage and features.
  * Does not exist in a VPC, in public zone.
  * A region failure would be needed to impact DynamoDB.
  * Replication between multiple nodes in multiple AZs.
  * True serverless DB as a Service.
  * Two billing items to remember:
    * Total amount of data stored by the product, all tables, all regions.
    * Performance demands:
      * Read capacity represents 4 KB of data
      * Write capacity represents 1 KB of data
    * Filtering does not reduce the capacity that is consumed.
      * It is the sort key that restricts the items returned, and reduces the capacity consumed.
  * In the exam preference a query operation.
    * Query can only ever query a single partition key.
  * A scan can check ranges.
  * **Table:**
    * A table is a grouping of items with the same primary key.
      * Simple (partition) or composite (partition and sort) primary key.
    * Each item must have a unique value for PK (primary key) and SK (sort key).
    * Can have none, all, mixture or different attributes (DDB has no rigid attribute schema).
    * Capacity (think speed) is set on a table.
    * Writes uses write capacity unit (WCU):
      * 1 WCU = 1KB per second.
    * Reads uses read capacity units (RCU):
      * 1 RCU = 4KB per second.
    * Max item size of 400KB
  * **Backups:**
    * **On-Demand:**
      * Full copy of table
        * Retained until removed.
        * Restore
          * Same or cross region
          * With or without indexes
          * Adjust encryption settings.
    * **Point-in-time Recovery:**
      * Enabled table by table
        * Not enabled by default
        * 1 second granularity
        * Continuous record of changes allows replay to any point in the window.
        * 35 day recovery window.
  * **Key Structure:**
    * Performance:
      * Over 10 GB = Partition is added.
      * Over 1000 write capacity units = Partition is added.
      * Over 3000 read capacity units = Partition is added.
        * Partitions cannot be removed.
    * Query non key values? Create an global secondary index.
    * DynamoDB can now be ATOMIC?
  * Reserved capacity can be purchased.
  **Advanced Info:**
    * Performance:
    * **Provisioned:**
      * Requires capacity planning.
      * More cost effective if you can determine the requirements.
    * **On-demand:**
      * No capacity planning required, pay for what you use.
      * Allows for no performance cap.
      * Can be more expensive.
    * **Global Tables:**
      * Requires streams and On-demand billing or autoscaling.
      * Global Tables enable you to use DynamoDB as a fully-managed, multi-region, multi-master database.
      * Last writer wins
      * **Local Secondary Index:**
        * Can only be created at the same time as the table.
        * Partition key must be same as base table.
        * Sort key consists of exactly one scaler attribute.
        * The base table's sort key is projected into the index, acting as a non-key attribute.
