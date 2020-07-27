# HPC and Placement Groups

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Placement groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html)

* **Notes:**
  * **Cluster placement group:**
    * Single AZ
      * Maximum possible performance between EC2 instances.
      * Benefits:
        * Highest levels of throughput
        * Lowest levels of latency
      * Capacity gets allocated in advanced.
    * **Partition placement group:**
      * EC2 attempts to distribute instances equally across partitions.
      * Large scale, replicated workloads where resilience is need.
    * **Spread placement group:**
      * Small set of infrastructure where you need highest level of availability.
      * Single AZ or multi AZ

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
