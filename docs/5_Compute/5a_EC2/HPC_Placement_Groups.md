# HPC and Placement Groups

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Placement groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html)

* **Notes:**
  * **Cluster placement group:**
    * Single AZ:
      * Cannot not span AZs.
      * Can span peered VPC, but impacts performance.
      * Maximum possible performance between EC2 instances.
      * Benefits:
        * Highest levels of throughput.
        * Lowest levels of latency.
      * Capacity gets allocated in advanced.
      * Use same type and launch time of EC2 instances.
    * **Partition placement group:**
      * EC2 attempts to distribute instances equally across partitions.
      * Large scale, replicated workloads where resilience is need.
      * 7 instances per AZ (HARD LIMIT).
      * Great for topology aware applications:
        * HDFS, HBase, Cassandra.
    * **Spread placement group:**
      * Small set of infrastructure where you need highest level of availability.
        * Each instances runes from a different rack.
        * Each rack has its own network and power source.
      * Single AZ or multi AZ.
      * 7 instances per AZ (HARD LIMIT)

* **Exam Tips:**
  * **Cluster placement group:**
    * Cannot really modify a placement group, have difficulty adding instances.
    * Better outcome when you provision the same type of instance.
    * Performance vs resilience? Cluster for performance.
    * Can span VPC peers, but do lose some benefits of extra bandwidth.
  * **Partition placement group:**
    * Large scale, replicated workloads where resilience is need.
  * **Spread placement group:**
    * Small set of infrastructure where you need highest level of availability.
