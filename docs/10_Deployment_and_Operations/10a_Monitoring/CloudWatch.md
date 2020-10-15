# CloudWatch

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [AWS Services That Publish CloudWatch Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html)
  * [Amazon S3 Server Access Log Format](https://docs.aws.amazon.com/AmazonS3/latest/dev/LogFormat.html)

* **Exam Tips:**
  * Namespace = Container for metrics e.g. AWS/EC2 or AWS/Lambda
  * Datapoint = Timestamp, value (optional) unit or measure.
  * Metric = Time ordered set of data points.
  * Alarms = Defined normal threshold conditions that can then take action based on the normal threshold being breached.
  **CloudWatch Logs:**
    * Public service used to store, monitor, and access logging data.
    * AWS, on-premise, IOT or any application.
    * CWAgent.
    * Route 53 Logging:
      * Only works for public hosted zones.
    * S3 Logging.
