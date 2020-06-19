# VPNs

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [AWS VPN Solutions](https://www.youtube.com/watch?v=qmKkbuS9gRs)

* **Exam Tips:**
  * When to use a VPN
  * Know the archictecture.
    * BGP required for dual vpn tunnels.
  * Can be done in minutes.
    * As opposed to direct-connect
  * Per hour cost.
  * Data cost for outbound data.
  * Generally limited by CGW.
  * Encrypted.
  * Performance is variable.
  * Route Table Priorities
    * (1.) Local route.
    * (2.) Static routes.
    * (3.) Direct Connect routes learned from BGP
    * (4.) Statically configured VPN route.
    * (5.) VPN routes learned from BPG
  * Quick to set up (possibly under an hour)
  * Virtual Private Gateway:
    * Actually physical
  * Max throughput of ~ 1.25Gbps
  * Latency considerations - inconsistent, public internet
  * Hourly cost, GB out cost, data cap (on premises)
  * Can be used as a backup for Direct Connect.
  * Can be used ontop of Direct Connect for security, providing encryption.
