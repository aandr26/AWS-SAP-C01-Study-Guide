# Kinesis Firehose

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Fully managed service to load data for data lakes, data stores, and analytics services.
  * Automatic scaling:
    * Fully serverless
    * Resilient
  * Near realtime delivery (~60 seconds)
    * Kinesis streams are realtime (~200 ms)
  * Supports transformation of data on the fly (lambda)
  * Billing - volume through firehose.
  * Supported destinations:
    * S3
    * Redshift
    * Elasticsearch
    * Splunk
  * Use Firehose when you need to take the data out of Kinesis.
