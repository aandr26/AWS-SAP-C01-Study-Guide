# Amazon Elastic MapReduce

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [About Amazon EMR Releases](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-release-components.html)
  * [Cluster Configuration Guidelines and Best Practices](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-instances-guidelines.html)
  * [Big Data on AWS](https://aws.amazon.com/big-data/use-cases/)

* **Exam Tips:**
  * EMR deployment options:
    * Cluster for specific funtion.
    * Create cluster to be long lasting for multiple workloads.
    * Cluster to be connected to and used interactively.
      * Run SQL like queries against hive.
  * Using S3 backed storage allows persistence of the data beyond the life of the cluster.
  * By default all instances in a cluster are place within the same AZ for performance.
  * Try to understand what Spark, Hive, and Pig do.
  * **EMR Cost and Performance Optimization:**
    * **Performance:**
      * Launch the cluster as close to the data source as possible, in the same region is perferable.
    * **Cost:**
      * Use lastest generations of the instance type.
      * Only use reserved instances _when_ you know the usage upfront.
