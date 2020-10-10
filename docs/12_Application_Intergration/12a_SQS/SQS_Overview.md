# SQS Architecture

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Public, Fully managed, highly-available queues - Standard or FIFO.
  * Messages up to 256KB in size - link to large data.
  * Received messages are hidden (VisibilityTimeout)
    * The messages either reappear (retry) or are explicitly deleted.
  * Dead-Letter queues can be used for problem messages.
  * Allows for distributed/decoupled application components.
  * ASG can grow based on queue size.
  * Lambda functions can replace the role of worker instances, polling and processing messages.
  * Default visibility timeout =
  * Message retention period =
  * Not designed for multiple consumers per queue.
    * Kinesis does allow multiple consumers.
  * Lookout for SQS fanout questions:
    * 1 SNS topic, with multiple subscribers (SQS queues) message will be added into each of the queues.
