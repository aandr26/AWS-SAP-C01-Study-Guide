# Lambda In-Depth

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Lambda function
    * It has it's own version v1, v2, v3 etc
      * A version is the code + the configuration of the lambda function.
      * Its immutable, it never changes once published and has its own ARN.
      * $Latest points at the latest version.
      * Aliases (DEV, STAGE, PROD) point at a version - can be changed.
  * Docker is an anti-pattern.
  * Runtimes supported include:
    * Python
    * Ruby
    * Java
    * Go
    * C#
    * Custom runtimes such as Rust are possible with Lambda Layers.
  * You directly control the memory allocated for Lambda functions whereas vCPU is allocated indirectly.
  * Function timeout of 900s (15 minutes).
    * Anything longer and you cannot use Lambda directly.
  * When connecting to a private VPC, Lambda creates ENIs within the target VPC.

  * **Logging:**
    * CloudWatch
    * CloudWatch Logs
    * X-Ray
    * Logs from Lambda executions go to CloudWatch Logs.
    * Lambda can be integrated with X-Ray for distributed tracing.
    * CloudWatch Logs requires permissions via Execution Role.
