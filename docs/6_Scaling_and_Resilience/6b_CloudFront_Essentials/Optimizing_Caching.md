# Optimizing Caching

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Configuring caching](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/ConfiguringCaching.html)

* **Exam Tips:**
  * Cache Hit = Matching object, delivered from cache
  * Cache Miss = Matching object not cached.
  * Maximize the cache hit ratio
  * ACM has to be provisioned in US-East-1 for global services like CloudFront.
  * Forward what the application needs
  * Cache based on what can change the objects
  * The more things are involved in caching the less efficient.
  * Cannot use self signed certificates.
  * Can change caching behavior based on:
    * cookies
    * selected request headers
    * query strings
  * Know the TTL values:
    * Default TTL = 24 hours
    * Can set minimum and maximum
  * Origin Headers:
    * Cache-Control max-age (seconds)
    * Cache-Control s-maxage (seconds)
    * Expires (Date & Time)
  * Cache invalidations:
    * Performed on a distribution
    * Applies to all edge locations - takes time
  * More frequent cache HITS = lower origin load
  * 304 Not Modified
  * 200 Ok
  * Versioned File names:
    * Logging
    * Caching
    * Consistency
    * Price
  