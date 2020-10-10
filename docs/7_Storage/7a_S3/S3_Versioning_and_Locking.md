# Versioning and Locking

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * **Versioning:**
    * Cannot disable versioning, can only suspend.
    * Unique ID per object, and with versioning a new unique ID is added for object per each new version.
    * If an object is deleted when versioning is enabled, it adds a delete marker, but does not delete the object itself or versions of the object.
      * Can delete the delete marker to see the object again in the console and cli.
    * Be aware that versioning exists and that you can refer to previous versions.
  * **Object Locking:**
    * Needs versioning enabled as well.
    * Can only be enabled at the time of creating a bucket.
      * Requires a support ticket to enable on existing buckets.
