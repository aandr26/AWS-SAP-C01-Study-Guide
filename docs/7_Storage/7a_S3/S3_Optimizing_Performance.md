# Optimizing S3 Performance

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Amazon S3 Transfer Acceleration — Speed Comparison](http://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html?region=us-east-1&origBucketName=secretcatpics)
  * [Request Rate and Performance Guidelines](https://docs.aws.amazon.com/AmazonS3/latest/dev/request-rate-perf-considerations.html)
  * [How Do I Enable Transfer Acceleration for an S3 Bucket?](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/enable-transfer-acceleration.html)
  * [Requirements for Using Amazon S3 Transfer Acceleration](https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html#transfer-acceleration-requirements)

* **Exam Tips:**
  * Standard vs Multipart Upload:
    * Should always preference multipart upload, faster and more reliable.

| Features | Standard | Multipart |
| -------- | -------- | --------- |
| **Size** | 5 GB     | 5 TB      |
| **Multithreading\***| No | Yes    |

  \* Multithreading helps maximize the bandwidth used to upload and decreases the impact to the network by reducing the size of the restart domains, it breaks the upload into smaller parts. It is akin to windowing.

  * **Partitions and Object Naming:**
    * Remember, no true folders.
    * S3 allows a mix of 3500 write TPS and 5500 read TPS per partition
      * If you don't need to achieve these results, don't worry about object naming in the bucket.
    * Prefixes determine the partioning of objects in a bucket.
