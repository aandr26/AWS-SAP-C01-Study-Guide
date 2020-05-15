# Amazon Relational Database Service (RDS)

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [IAM Database Authentication for MySQL and PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.html#UsingWithRDS.IAMDBAuth.Availability)
  * [Enabling and Disabling IAM Database Authentication](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.Enabling.html)
  * [How do I allow users to connect to Amazon RDS with IAM credentials?](https://aws.amazon.com/premiumsupport/knowledge-center/users-connect-rds-iam/)
  * [What's New in Amazon Relational Database Service](https://www.youtube.com/watch?v=HuvUD7-RyoU)
  * [Tutorials Dojo RDS Cheat Sheet](https://tutorialsdojo.com/amazon-relational-database-service-amazon-rds/)

* **Exam Tips:**
  * Most use cases, General Purpose SSD is fine.
  * Have knowledge of backup retention period.
  * **Backups:**
    * Saved to S3, where it is then replicated.
    * **Automatic backups:**
      * For true Point-in-Time recovery.
      * It is done using transaction logs in automatic backups.
    * Snapshots
  * **Replication:**
    * Replication is between master and slave node.
    * No access to slave node when the master node is working.
    * No storage replication.
  * **Payment methods:**
    * On-demand
    * Reserved:
      * All upfront
      * Partial upfront
      * No upfront
      * Terms 1-3 yrs
  * New database can be created using a snapshot.
  * **Read Replicas:**
    * Can be deployed to another AZ, or even another region.
    * Good for read intensive applications.
    * Can be addressed directly as opposed to a slave node.
    * Is a completely DB instance
    * Can have a different DB version.
