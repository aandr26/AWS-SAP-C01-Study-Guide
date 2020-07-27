# EC2 Networking

* [Return to table of contents](../../../README.md)

* **Exam Notes:**
  * The primary ENI cannot be detached from one instance and connected to another.
  * You can have multiple interfaces attached to an instance, and those interfaces can be in different subnets, but not in different AZs.
  * IP addresses are associated with interfaces, not instances. A secondary interface can be moved from one instance to another.
  * A public IP address, either from the subnet or explicitly defined while launching, is not configured on the OS. It is allocated to the instance.
  * An Elastic IP address will override the public IP, and if unallocated, the public IP will be different.
  * Source and destination check is a per interface option.
