# Glacier Architecture

[Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Amazon S3 Glacier Data Retrieval Policies](https://docs.aws.amazon.com/amazonglacier/latest/dev/data-retrieval-policy.html)
  * [Retrieving Vault Metadata in Amazon S3 Glacier](https://docs.aws.amazon.com/amazonglacier/latest/dev/retrieving-vault-info.html)
  * [Downloading a Vault Inventory in Amazon S3 Glacier](https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-inventory.html)
  * [Amazon S3 Glacier Vault Lock](https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html)
  * [Working with Archives in Amazon S3 Glacier](https://docs.aws.amazon.com/amazonglacier/latest/dev/working-with-archives.html)

* **Exam Tips:**
  * Historically it was technically its own product.
  * Used for long-term archival storage.
  * Vaults contain archives.
  * Accounts can contain 1000 vaults per region.
  * Descriptions can only be added to an archive _when_ it is uploaded!
  * There are no user-defined metadata fields. Only unique ID plus optional description. See above for description restrictions.
  * _Cannot_ be edited, only deleted and reuploaded.
    * Recieves a new unique ID.
  * Cannot see data within the archive.
  * Speeds:

| Speed Type | Time to complete |
|----------- | ---------------- |
| Expedited  | 1-5 Minutes\*    |
| Standard   | 3-5 Hours        |
| Bulk\*\*   | 5-12 Hours       |

\* For anything below 250 MB archives.
\*\* Best economic option for large jobs.
