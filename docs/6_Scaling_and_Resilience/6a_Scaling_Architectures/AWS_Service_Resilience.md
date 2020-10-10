# AWS Service Resilience

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * **IAM:**
    * Globally resilient.
  * **S3:**
    * Regional level.
    * Replicated across AZs in region.
  * **Route 53:**
    * Operates name servers from edge locations positioned globally.
    * Separate from regions.
* **Compute:**
  * **EC2/EBS:**
    * EC2 limited to a single AZ.
      * If AZ fails, probably lose the instance.
    * EBS in AZ:
      * Some replication within same AZ.
      * Snapshots use S3 as backend, and replicated across all AZs in region.
      * Can also copy a snapshot to another region.
    * **ELB:**
      * Regional.
      * Network interfaces are placed in subnets in different AZs.
    * **ASG:**
      * Regional
      * If configured for all AZs in one region, the ASG can provision instances in any working AZs within the region in case of a failure in any given AZs.
* **Networking:**  
  * **VPC:**
    * VPC is regional
      * Subnets cannot span AZs.
        * Neither can the services deployed inside a single subnet.
        * Put one subnet per AZ.
  * **NAT GW:**
    * Not resilient by default.
    * Placed in a subnet, thus they are AZ bound.
    * Can tolerate hardware failures.
  * **VPN:**
    * VPGW:
      * Publicly available
      * In multiple AZs (Think dual tunnel).
