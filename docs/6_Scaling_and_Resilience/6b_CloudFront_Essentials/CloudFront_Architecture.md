# CloudFront Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Origin Failover](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html)
  * [Tutorial Dojo CloudFront](https://tutorialsdojo.com/amazon-cloudfront/)

* **Exam Tips:**
  * ACM has to be provisioned in US-East-1 for global services like CloudFront.
  * Cannot use self signed certificates.
  * Questions involving Adobe Flash Media Server RTMP require S3 and RTMP distribution type.
  * Can be integrated with WAF.
  * Older browsers? Dedicated IP address for each edge location.
  * Can specify restrict view access.
    * Per-behavior setting.
  * Can create origin failover by creating an origin group with two origins:
    * One acts as the primary origin.
    * The other origin acts as the secondary which CloudFront will switch to in the case of the primary failing.
    * CloudFront is for downloads only. Any uploads go directly to the origin.
