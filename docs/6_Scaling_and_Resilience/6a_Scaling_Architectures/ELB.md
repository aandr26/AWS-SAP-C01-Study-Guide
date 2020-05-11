# Elastic Load Balancers

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Compare](https://aws.amazon.com/elasticloadbalancing/features/#compare)
  * [Network introduction](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html)
  * [Authenticate users](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html)
  * [Application introduction](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html)
  * [Classic introduction](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/introduction.html)
  * [Elastic Load Balancing: Deep Dive and Best Practices](https://www.youtube.com/watch?v=VIgAT7vjol8)

  * **Exam Tips:**
    * Need to know what scenario to use specific types of ELBs.
    * Provides abstraction.
    * ELBs allow decoupling of the tiers.
    * **Classic Load Balancer:**
      * Not recommended
      * Not layer 7 device.
      * Can do SSL offloading by having the LB do the SSL/TLS work, freeing up some work on the instances.
    * **Application Load Balancers:**
      * Recommended LB to use within VPCs.
      * Supports both IPv4 and IPv6 using dualstack.
      * Associate target groups.
      * Understand up to layer 7 in the OSI model.
      * Does allow you to provide multiple success codes.
      * Almost always cheaper.
      * Can make routing decisions via rules:
        * Forward
        * Redirect
        * Authenticate
      * Can cope with multiple certificates.
      * HTTP/2 is supported.
      * Can have lambda functions as targets.
      * Healthchecks defined at target group level.
    * **Network Load Balancers:**
      * Operate at layer 4 of the OSI model.
      * TLS termination supported.
      * UDP and TCP both supported.
      * End-to-end encryption? = NLB
