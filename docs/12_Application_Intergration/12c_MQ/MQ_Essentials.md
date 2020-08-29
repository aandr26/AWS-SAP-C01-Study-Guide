# Amazon MQ Overview

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Amazon MQ Network of Brokers](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/network-of-brokers.html)
  * [Amazon MQ Features](https://aws.amazon.com/amazon-mq/features/)
  * [Getting Started with Amazon MQ](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/amazon-mq-getting-started.html)

* **Exam Tips:**
  * Message broker.
  * Can function as a Queue or Topic.
  * Supports JMI API, AMQP, MQTT, OpenWire or STOMP
  * Not controllable with AWS security or APIs.
  * **Use Cases:**
    * For scenarios where a messaging system is already developed and needs to be moved to the cloud.
    * Default to SNS or SQS for most new implementations.
    * SNS or SQS if AWS integration is required (logging, permissions, encryption, service integration.)
    * Used Amazon MQ if you need to use JMI API, AMQP, MQTT, OpenWire or STOMP.
