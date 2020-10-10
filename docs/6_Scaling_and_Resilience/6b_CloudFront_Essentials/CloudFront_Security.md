# CloudFront Security

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Requirements for using SSL/TLS certificates](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cnames-and-https-requirements.html)
  * [Restricting Access to Amazon S3 Content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html)
  * [Using signed URLs](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-urls.html)
  * [Using CloudFront geo restrictions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html#georestrictions-cloudfront)
  * [Using a third-party Geolocation service](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html#georestrictions-geolocation-service)
  * [Using field-level encryption](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html)

* **Exam Tips:**
  * **SSL:**
    * Supported by default.
    * Using CNAME:
      * Verify ownership (optionally HTTPS) using a matching cert.
      * Can use with ACM, but the cert must be requested for the US East (N. Virginia) region.
      * Two SSL connections:
        * Viewer => CloudFront and CloudFront => Origin
        * _Both need valid public certs and intermediate certs._
      * SNI mode is free, doesn't support old, old browsers.
      * Can pay for a dedicated IP per distribution.
  * Be aware of the security requirements for SSL:
    * Not a single connection:
      * Viewer connection to edge location.
        * Cannot use a self-signed certificate.
        * Must use publicly trusted and valid cert.
      * **Origin:**
        * If S3, automatic, if ELB, can use ACM.
          * ACM is a regional service, and must be provisioned in US-East-1 region.
        * If using on-premises server, Must use publicly trusted and valid cert.
    * Does nothing by default to restrict access to an S3 DNS endpoint.
      * Can restricted use an Origin Access Identity (OAI)
    * Be aware of how to configure signed URLs:
      * It is configured _per_ behavior - _not distribution_.
      * For a single behavior cannot have signed URLs and public access at same time.
      * Trusted signer? Assume it is private!
      * Cannot use signed URLs using RTMP!
    * Field level encryption:
      * Insist any communication are encrypted using specific key pair.
    * **Geo Restriction:**
      * CloudFront georestriction and is based solely on the location of the IP address.
        * Country Only!
          * Country code.
        * Distribution level
        * Whitelist or Blacklist at the country level.
      * 3rd party geolocation, using SignedURLs, can be much more accurate.
        * Uses signed URLs or cookies using a compute instance.
        * Can be use to restrict based on almost anything (licensing, user login status, user profile fields and much more)
        * Anything beyond the country.
    * **Origin Access Identity (OAI):**
      * An OAI is a type of identity.
      * Can be associated with CloudFront Distributions.
      * CloudFront 'becomes' that OAI.
      * That OAI can be used in S3 bucket policies.
      * Deny all but one or more OAIs.
    * **Private Distributions:**
      * Public - open access to objects.
      * Private - requests require signed cookie or URL.
      * 1 behavior - Whole distribution public or private.
      * Multiple behaviors - each is public or private.
      * A CloudFront Key is created by an account root user.
      * That account is added as a trusted signer.
      * Signed URLs:
        * URL provides access to one object.
        * Legacy RTMP distributions can't use cookies.
        * Use URLs if your client doesn't support cookies.
        * Cookie provides access to groups of objects.
        * Use for groups of files/all files of a type.
        * Or if maintaining URLs is important.

Example bucket policy using OAI

```JSON
{
    "Version": "2008-10-17",
    "Id": "PolicyForCloudFrontPrivateContent",
    "Statement": [
        {
            "Sid": "1",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::cloudfront:user/USERNAME"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::bucketname/*"
        }
    ]
}
```
