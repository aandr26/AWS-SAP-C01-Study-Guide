# DynamoDB Operations, Consistency, and Performance

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * **On-Demand Model:**
    * Used when usage is unknown, unpredictable, allows for low admin tasks.
    * Priced for per million R or W units.
  * **Provisioned Model:**
    * RCU and WCU set on a per table instance.
    * Every operation consumes at least 1 RCU/WCU(*)
  * 1 RCU is 1 x 4KB read operation per second.
  * 1 WCU is 1 x 1KB write operation per second.
  * Every table has a RCU and WCU burst pool (300 seconds)
  * **Operations:**
    * **Query:**
      * Most efficient operation in DynamoDB
      * Query accepts a single PK value and optionally a SK or range.
      * Capacity consumed is the size of all returned items. Further filtering discards data - capacity is still consumed.
      * Can only query on a PK or PK and SK.
      * Formula example:
        * 2.5KB + 1.5KB = 4KB = 1 RCU
        * 2.5KB = 1 RCU
      * More efficient to poll for multiple items using a single query.
    * **Scan:**
      * Least efficient way to get an item.
      * Scan moves through a table consuming the capacity of every item.
      * You have the complete control on what data is selected, any attributes can be used and any filters applied but scan consumes capacity for every item scanned through.
  * **Consistency:**
    * 1). Item updated, i.e. removing an attribute.
    * 2). DynamoDB directs the write at the leader storage node. Which is elected from the three storage nodes.
    * 3). The leader node replicates data to other nodes, typically finishing within a few milliseconds.
    * 4). Eventually consistent reads check 1/3 nodes.
    * 5). Strongly consistent reads connect to the leader node to the the most up-to-date copy of data.
  * **WCU Calculation:**
    * If you need to store 10 items per second 2.5KB average size per item. (Look out for exam questions that say minutes instead of seconds.)
      * Calculate WCU per item by rounding up (item size / 1 KB) = 3
      * Multiply by average number per second (30)
      * = 30 WCU
  * **RCU Calculation:**
    * If you need retrieve 10 items per second 2.5KB average size per item. (Look out for exam questions that say minutes instead of seconds.)
      * Calculate RCU per item by rounding up (item size / 4 KB) = 1
      * Multiply by average read ops per second (10)
      * = strongly consistent 10 RCU
      * 50% of strongly consistent = eventually consistent 10 RCU required 10
  * **DAX:**
    * Primary node (writes) and replicas (read)
    * Nodes are HA
      * Primary failure = election
    * In-mem cache
      * scaling much faster reads, reduced costs.
    * Scale up ands scales out (bigger or more).
    * Supports write-through
    * DAX deployed within a VPC
