# Kinesis

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Kinesis FAQ](https://aws.amazon.com/kinesis/data-streams/faqs/)
  * [Configuring Application Input](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-input.html)
  * [Continuous Queries](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/continuous-queries-concepts.html)
  * [Windowed Queries](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/windowed-sql.html)
  * [Example Applications](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/examples.html)

* **Exam Tips:**
  * Designed for huge scale ingestion.
  * Multiple consumers, 24 hour rolling window.
  * Data ingestion, analytics. monitoring, app clicks.
  * **Producers:**
    * Anything which puts data into Kinesis.
      * Android/iPhone
      * Software
      * EC2 instance(s)
  * **Consumers:**
    * Consumes and uses the records from a Kinesis stream.
      * EC2 instance(s) running the Kinesis Consumer Library (KCL).
      * Lambda functions
      * Kinesis Firehose
  * Producers -> Stream -> Consumers
  * Can scale to any load that is required.
  * **Streams:**
    * Data Streams:
      * 24 hours retention period by default - up to 7 days (extended data retention) and up to 365 days (long-term data retention) at an extra cost.
      * Each shard = 1 MB across all producers, 2 MB across all consumers.
      * Uneven write pattern, when you don't reach the total performance of a stream.
      * Can configure shard level metrics at extra cost.
      * Private only vpc? Need to us a Kinesis endpoint to access public resources.
  * **Data Analytics:**
    * Use cases:
      * Time-series analytics
      * Realtime dashboards
      * Realtime metrics
      * Complex manipulation of data in realtime.
    * Allows SQL queries against realtime data streams.
      * Create dashboards or alerts.
    * Destinations:
      * S3
      * Redshift
      * ElasticSearch
      * Splunk
      * Firehose (makes it near realtime)
    * Understand:
      * Reference table.
      * In application input and output.
      * Different products that can be used as inputs.
      * You can define an error stream.
