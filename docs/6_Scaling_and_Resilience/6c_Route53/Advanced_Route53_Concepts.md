# Advanced Route 53 Concepts

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Routing Policy](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html)
  * [Traffic Flow](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/traffic-flow.html)
  * [Traffic Policies](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/traffic-policies.html)
  * [Multivalue vs Simple Policies](https://aws.amazon.com/premiumsupport/knowledge-center/multivalue-versus-simple-policies/)

* **Exam Tips:**
  * VPC interfaces (ENIs) - Accessible over VPN or DX.
  * Inbound Endpoints:
    * on-prem can forward to R53 resolver
  * Outbound Endpoints:
    * conditional forwarding of requests from R53 to on-prem.
  * Rules control what requests are forwarded.
