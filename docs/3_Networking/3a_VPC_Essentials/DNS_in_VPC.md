# DNS in a VPC

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Resolving DNS queries between VPCs and your network](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html)
  * [Introduction to Amazon Route 53 Resolver for Hybrid Cloud](https://www.youtube.com/watch?v=D1n5kDTWidQ)

* **Exam Tips:**
  * Route 53 inbound endpoint
    * Allow on-premise networks to connect to the Route 53 resolver which operates on the network +2 address.
  * Route 53 outbound endpoint
    * Allows resources within AWS VPCs to resolve specific queries against on-premise DNS servers.
