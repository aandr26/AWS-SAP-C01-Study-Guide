# Amazon Elastic MapReduce

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [About Amazon EMR Releases](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-release-components.html)
  * [Cluster Configuration Guidelines and Best Practices](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-instances-guidelines.html)
  * [Big Data on AWS](https://aws.amazon.com/big-data/use-cases/)

* **Exam Tips:**
  * Used for big data processing, manipulation, analytics, indexing, transformation, and more (used as a part of data pipeline).
  * If these are mentioned in the exam, EMR is probably being used:
    * Spark
    * HBase
    * Presto
    * Fink
    * Hive
    * Pig
  * EMR deployment options:
    * Cluster for specific function.
    * Create cluster to be long lasting for multiple workloads.
    * Cluster to be connected to and used interactively.
      * Run SQL like queries against hive.
  * Using S3 backed storage allows persistence of the data beyond the life of the cluster.
  * By default all instances in a cluster are place within the same AZ for performance.
  * Try to understand what Spark, Hive, and Pig do.
  * **EMR Architecture:**
    * Each cluster has at least 1 node - the master node.
      * Master node manages the cluster and its health.
      * It distributes workloads, and acts as the NAME node within MapReduce.
      * The node you SSH into.
    * Clusters can have zero or more core nodes.
      * Act as data nodes for HDFS.
      * Run task trackers and can run mapping and reduce tasks in the cluster.
    * Task nodes are optional:
      * They have no HDFS involvement.
      * They don't rune task trackers (core), only run tasks.
      * Ideal for SPOT based scaling.
  * **EMR Cost and Performance Optimization:**
    * **Performance:**
      * Launch the cluster as close to the data source as possible, in the same region is preferable.
    * **Cost:**
      * Use latest generations of the instance type.
      * Only use reserved instances _when_ you know the usage upfront.
      * If you are using per-second billing, it might make more sense to run more instances for a shorter amount of time to process jobs quicker.
        * The logic behind this is that since the hour minimum billing is no longer applicable, you can use more instances to process a job quicker and pay the same price or less.
