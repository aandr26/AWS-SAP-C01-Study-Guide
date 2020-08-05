# VPC Flow Logs

* [Return to table of contents](../../../README.md)

* Useful Links:
  * [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html)

* **Exam Tips:**
  * Flow Logs only provide access to the traffic metadata, not the actual IP traffic itself.
  * What is logged:
    * Default format:
      * version
      * account-id
      * interface-id
      * srcaddr
      * dstaddr
      * srcport
      * dstport
      * protocol
      * packets
      * bytes
      * start
      * end
      * action
      * log-status
  * What isn't logged:
    * DHCP.
    * AWS DNS.
    * Meteadata.
    * License Activation Requests.
  * Destinations:
    * CWLogs.
    * S3 Buckets.
  * Possible misaligned NACL and security groups, if you see multiple accept and reject entries.
