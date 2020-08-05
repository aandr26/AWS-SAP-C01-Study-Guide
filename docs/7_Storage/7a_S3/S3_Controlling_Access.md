# Controlling Access to S3 Buckets

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Bucket Policy Examples](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html)
  * [Uploading Objects Using Presigned URLs](https://docs.aws.amazon.com/AmazonS3/latest/dev/PresignedUrlUploadObject.html)

* **Exam Tips:**
  * Private by default
  * Tags and resource policies can work together to grant extensive permissions.
  * Questions about object specific permissions and access via a URL, define an object level ACL.
  * **Pre-Signed URLs:**
    * Uses the identity of the user who created the pre-signed URL.
    * When using a pre-signed url, the user does not need to have currently valid permissions to access the object.
    * Has an expiration.
    * Generally used by applications within AWS to provide specific permissions.
      * Think of someone purchasing an image and than being given a pre-signed URL to download the image from S3 for a limited amount of time.
      * The point of creating the URL is when the permissions are checked and applied, and when using the URL in the future the permissions of the URL are checked.
