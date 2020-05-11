# DynamoDB Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [General Guidelines for Secondary Indexes in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-indexes-general.html)
  * [Read Consistency](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadConsistency.html)

* **Exam Tips:**
  * True serverless DB as a Service.
  * Two billing items to remember:
    * Total amount of data stored by the product, all tables, all regions.
    * Performance demands:
      * Read capacity represents 4 KB of data
      * Write capacity represents 1 KB of data
    * Filtering does not reduce the capacity that is consumed. 
      * It is the sort key that resricts the items returned, and reduces the capacity consumed.
  * In the exam preference a query operation.
    * Query can only ever query a single partition key.
  * A scan can check ranges.
  * Key Structure:
    * Performance:
      * Over 10 GB = Partition is added.
      * Over 1000 write capacity units = Partition is added.
      * Over 3000 read capacity units = Partition is added.
        * Partitions cannot be removed.
    * Query non key values? Create an global secondary index.
    * DynamoDB can now be ATOMIC?
  * Reserved capacity can be purchased.
