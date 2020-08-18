# AWS Batch

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * AWS managed 'Batch Processing' product.
  * Batch processing:
    * Jobs that can run without end user interaction or can be scheduled to run as resources permit.
  * AWS Batch lets you worry about defining jobs by handling the underlying computer and orchestration.
  * **Batch Components:**
    * **Job:**
      * Script, executable or Docker container submitted to Batch.
        * The thing to run.
        * Can be dependant on other jobs
    * **Job definition:**
      * Metadata for a job.
        * Including permissions (IAM), resource config, mount points.
    * **Job Queue**
      * Jobs are submitted to a queue where they wait for compute environment capacity.
      * Queues are associated with 1+ compute environments.
    * Compute environment - managed or unmanaged compute
      * Where you configure instance type/size, vCPU amount, spot price.
      * Or define another compute environment used in ECS
  * **Batch vs Lambda:**
    * **Lambda:**
      * 15 minute execution time limit.
      * Limited disk space in the environment.
      * EFS access fixes this but means VPC lambda.
      * Fully serverless but limited runtime selection.
    * Batch:*** Not serverless, it uses docker, allowing any runtime.
      * No time limit or effective resource limit.
  * **Managed vs Unmanaged:**
    * **Managed:**
      * AWS Batch manage capacity based on workloads.
      * On-demand or spot instance - size/type
      * You can determine max spot price.
      * VPC private/public, requires VPC gateways.
    * **Unmanaged:**
      * You managed everything!
