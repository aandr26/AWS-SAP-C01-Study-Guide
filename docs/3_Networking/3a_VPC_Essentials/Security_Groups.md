# Security Groups

* [Return to table of contents](../../../README.md)

* **Notes:**
  * Stateful:
    * No ability to restrict returning traffic.
  * Filtering, applied to network interfaces.
  * Applied when traffic goes in or out of an interface.
  * No order processing.
  * Default allow all outbound traffic.

* **Exam Tips:**
  * Not able to explicitly deny traffic.
  * Does not work on DNS names:
    * Logical resources
    * IPs
    * CIDR ranges
  * Unless explicitly allowed, there is a hidden implicit deny.
  * Any other logical resources can be referenced.
  * Able to add functional, role based security.
  * You can use the CLI to export the definitions of a SG that you can than use to make a new security group in another region.
