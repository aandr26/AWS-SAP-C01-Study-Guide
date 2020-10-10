# Creating and Working with Distributions

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Optimizing high availability](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html)
  * [Supported protocols and ciphers](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/secure-connections-supported-viewer-protocols-ciphers.html)

* **Exam Tips:**
  * Older browsers (don't support SNI) support comes at additional costs.
  * Memorize supported policies.
  * ACM has to be provisioned in US-East-1 for global services like CloudFront.
  * Cannot use self signed certificates.
  * **Behaviors:**
    * Price class.
    * AWS WAF web ACL.
    * Alternate Domain Names (CNAMEs).
      * Custom domain name = custom cert.
    * Viewer protocol policy:
      * HTTP and HTTPS or mixture of both or one or the other.
    * Caching controls.  
    * Restrict view access.
