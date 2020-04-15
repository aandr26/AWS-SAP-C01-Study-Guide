# Network Access Control Lists (NACLs)

* **Useful Links:**
  * [Wikipedia Ephemeral Port article](https://en.wikipedia.org/wiki/Ephemeral_port)

* **Notes:**
  * Processing starts in order from the lowest number to the higher.
    * ie, 100 before 110
  * Once a rule matches, it applies the rule and stops.
  
* **Exam Tips:**
  * Subnets can only be associated with one NACL
  * Stateless
  * Exam gotcha, troubleshoot connectivity between EC2 instances in the same subnet, a NACL does not restrict this.
  * Traffic within a subnet, EC2 instance to EC2 instance, would not be affected. It only affects traffic that crosses a subnet boundary.