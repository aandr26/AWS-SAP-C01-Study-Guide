# Custom Origins

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Customize the protocols used between edge location and origin? Must use custom origin.
  * Any custom origins you use need a public IP address.
  * ACM has to be provisioned in US-East-1 for global services like CloudFront.
  * Cannot use self signed certificates.
  * Look for these clues:
    * Minimum Origin SSL Protocol
    * Origin Protocol Policy
    * Change ports
