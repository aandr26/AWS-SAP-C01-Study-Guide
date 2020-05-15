# CloudFront Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Origin Failover](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html)

* **Exam Tips:**
  * Questions involving Adobe Flash Media Server TRMP require S3 and RTMP distribution type.
  * Can be integrated with WAF
  * Older browsers? Dedicated IP address for each edge location.
  * Can specify restrict view access.
    * Per-behavior setting.
  * Can create origin failover by creating an origin group with two origins:
    * One acts as the primary origin
    * The other origin acts as the secondary which CloudFront will switch to in the case of the primary failing.
