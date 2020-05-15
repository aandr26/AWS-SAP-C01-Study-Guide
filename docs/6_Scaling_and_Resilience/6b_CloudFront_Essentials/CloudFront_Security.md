# CloudFront Security

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Requirements for using SSL/TLS certificates](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cnames-and-https-requirements.html)
  * [Restricting Access to Amazon S3 Content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html)
  * [Using signed URLs](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-urls.html)
  * [Using CloudFront geo restrictions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html#georestrictions-cloudfront)
  * [Using a third-party geolocation service](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html#georestrictions-geolocation-service)
  * [Using field-level encryption](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html)

* **Exam Tips:**
  * Can use with ACM, but the cert must be requested for the US East (N. Virginia) region.
  * Be aware of the security requirements for SSL:
    * Not a single connection:
      * Viewer connection to edge location.
        * Cannot use a self-signed certificate.
        * Must use publicaly trusted and valid cert.
      * Origin:
        * If S3, automatic, if ELB, can use ACM.
        * If using on-premises server, Must use publicaly trusted and valid cert.
    * Does nothing by default to restrict access to an S3 dns endpoint.
      * Can restricted use an Origin Cccess Identity (OAI)
    * Be aware of how to configure signed URLs:
      * It is configured _per_ behavior - _not distribution_.
      * For a single behavior cannot have signed URLs and public access at same time.
      * Trusted signer? Assume it is private!
      * Cannot use signed URLs using RTMP!
    * Geo Restriction:
      * Distribution level
      * Whitelist or Blacklist at the country level.
      * CloudFront geo restriction and is based soley on the location of the IP address.
      * 3rd part geo restriction, using SignedURLs, can be much more accurate.
    * Field level encryption:
      * Insist any communication are encrypted using specific key pair.

Exmample bucket policy using OAI

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
