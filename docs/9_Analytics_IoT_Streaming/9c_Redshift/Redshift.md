# Amazon Redshift Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Deep Dive and Best Practices for Amazon Redshift](https://www.youtube.com/watch?v=TJDtQom7SAA)
  * [Distribution Styles](https://docs.aws.amazon.com/redshift/latest/dg/c_choosing_dist_sort.html)

* **Exam Tips:**
  * Can support up to 2 PB of data.
  * OLAP (Column based) not OLTP (row/transaction).
  * Pay as you go.
  * **Redshift Architecture:**
    * Server based (not serverless).
    * One AZ in a VPC - network cost/performance.
    * Leader node - Query input, planning and aggregation.
    * Compute node - performing queries of data.
    * Redshift enhanced VPC routing - VPC networking.
    * Automatic snapshots to S3 (8 hours or 5GB) with retention.
      * Default retention of 1 day, with up to 35 days.
    * Manual snapshots to S3 managed by administrator.
  * **Resizing:**
    * Classic resize:
      * Change both node type and number of nodes.
    * Elastic resize:
      * Only change number of nodes.
  * Be aware of the services that Redshift can interact with:
    * Kinesis
    * S3
    * Data pipelines
  * Can copy automatic and manual snapshots to a destination region, and they have independent retention periods.
