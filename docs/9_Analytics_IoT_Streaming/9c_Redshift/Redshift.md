# Amazon Redshift Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Deep Dive and Best Practices for Amazon Redshift](https://www.youtube.com/watch?v=TJDtQom7SAA)
  * [Distribution Styles](https://docs.aws.amazon.com/redshift/latest/dg/c_choosing_dist_sort.html)

* **Exam Tips:**
  * Can support up to 2 PB of data.
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
