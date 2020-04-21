# VPNS

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
