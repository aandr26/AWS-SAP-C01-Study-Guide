# RDS Backups and Restores

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * First snapshot is full.
    * Following snaps are incremental.
  * Automatic backups:
    * 5 minute transaction logs.
    * Can set retention period between 0 - 35 days.
    * Saved in AWS managed S3.
  * Restores:
    * Creates new RDS instance with new endpoint address.
    * Automated = any 5 minute point in time.
    * Backup is restored and transaction logs are 'replayed' to bring DB to desired point in time.
    * Restores aren't fast - think about RTO.
