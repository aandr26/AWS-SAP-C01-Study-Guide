# ECS Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Example task definitions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/example_task_definitions.html)
  * [Linux Academy ECS Deep Dive course](https://linuxacademy.com/cp/modules/view/id/261)
  * [Deep Dive on Amazon EKS](https://www.youtube.com/watch?v=EDaGpxZ6Qi0)

* **Exam Tips:**
  * Windows container host:
    * NAT is only supported networking mode.
  * Container definition:
    * where a container is
    * which port to use
  * Task definition:
    * Resources
    * Networking
    * Instance type - EC2 vs Fargate
    * The task role, what it does.
      * IAM Role
  * Service:
    * How many copies
    * HA
    * Restarts
  * **Use Case:**
    * If you use containers = ECS
    * Large workload - price conscious = EC2 Mode
    * Large workload - overhead conscious = Fargate
    * Small / Burst workloads = Fargate
    * Batch / Periodic workloads = Fargate
