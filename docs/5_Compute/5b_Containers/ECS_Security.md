# ECS Security

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Using AWS logs](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_awslogs.html)
  * [IAM roles for tasks](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html)

* **Exam Tips:**
  * If asked about how to restrict traffic to an individual container, choose ECS network only mode.
  * **Fargate:**
    * Secure tasks only
  * **Instance type:**
    * Hosts
    * Tasks
      * ECS agents not working correctly?
        * Check the instance role.
