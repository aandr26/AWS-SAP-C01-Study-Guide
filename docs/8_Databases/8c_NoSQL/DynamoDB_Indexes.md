# DynamoDB Indexes

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Indexes are alternative views on table data.
  * Different SK (Local Secondary Indexes) or different PK and SK (Global Secondary Indexes).
  * Some or all attributes (projection).
  * **Local Secondary Indexes (LSI):**
    * Must be created when the table is created.
    * 5 LSIs per table
    * Alternative SK, same PK.
    * Shares the RCU and WCU wit the table when using provisioned capacity.
    * Attributes - ALL, KEYS_ONLY, and INCLUDE
  * **Global Secondary Indexes:**
    * Can be created at any time.
    * Limit of 20 per base table.
    * Alternative PK and SK.
    * Does not support strongly consistent reads.
    * GSIs have their own RCU and WCU allocations.
    * Attributes - ALL, KEYS_ONLY, and INCLUDE
    * Generally sparse as only items that have values in the new PK and optional SK are added.
  * Considerations:
    * Careful with projects (KEYS_ONLY, INCLUDE, ALL)
    * Queries on attributes NOT projected are expensive.
    * Use GSIs as default, LSI only when strong consistency is required.
    * Use indexes for alternative access patterns.
