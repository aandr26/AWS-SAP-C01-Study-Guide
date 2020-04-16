# Security Groups

* **Notes:**
  * Stateful:
    * No ability to restrict returning traffic.
  * Filtering, applied to network interfaces.
  * Applied when traffic goes in or out of an interface.
  * No order processing.
  * Default allow all outbound traffic.

* **Exam Tips:**
  * Not able to explicity deny traffic.
  * Unless explicitly allowed, there is a hidden implicit deny.
  * Any other logical resources can be referenced.
  * Able to add functional, role based security.
