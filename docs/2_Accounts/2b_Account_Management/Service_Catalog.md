# AWS Service Catalog

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Service Catalog](https://aws.amazon.com/servicecatalog/faqs/)

* **Exam Tips:**
  * There's a requirement for endusers to deploy products that they don't have permissions to do otherwise, in a self-service way.
  * Used to tag provisioned resources with corresponding unique identifiers for portfolio, product, and users.

If you want to give your enduser permission to luanch a product you need this policy created and attached.

```JSON
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "servicecatalog:ProvisionProduct"
                ],
                "Resource": "*"
        }
    ]
}
```
