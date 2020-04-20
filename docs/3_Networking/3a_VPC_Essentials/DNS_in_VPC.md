# DNS in a VPC

* Useful Links:
  * [Resolving DNS queries between VPCs and your network](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html)

* **Notes:**
  * Route 53 inbound endpoint
    * Allow on-premise networks to connect to the Route 53 resolver which operates on the network +2 address.
  * Route 53 outbound endpoint
    * Allows resources within AWS VPCs to resolve specific queries against on-premise DNS servers.
