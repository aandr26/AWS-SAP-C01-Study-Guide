# Data Persistence

## Emphemeral

Data this is local to a resource (usually) and lost when the resource is powered off.

* Examples:
  * Instance Store Volume
  * Amazon ElastiCache

* Notes:
  * Very high throughput.
  * Data is *lost* when the resource is powered down.
    * Data does survive a reboot, but if an instance is terminated or the disk itself fails, the data is lost.

## Persistent

Data that is durable and able to survive power events such as start, stop, and restart.

* Examples:
  * Amazon EBS (Elastic Block Store)
  * Amazon EFS (Elastic File Store)

* Notes:
  * Comes at an extra cost
  * Not default.
  * Good for things such as databases.

## Transient

Datastores that exist with the intention that the data injected is temporary.

* Examples:
  * SQS

* Notes:
  * Not used for permanent storage.
  * Used as intermediaries between services.
