# Public vs. Private Subnets, Internet Gateways, and IP Addressing

* **Notes:**
  * Bastion hosts

* **Exam Tips:**
  * The bastion host does not have a public IP, it is the IGW that handles the public IP.
  * NAT Gateways allow private resources to connect out. Do not provide any form of incoming access apart from returning traffic.
  * NAT Gateways do scale with load.
  * IGW for IPv4 and IPv6 public routable traffic.
  * Use NAT gateway for private IPv4 outbound to public internet.
