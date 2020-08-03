# AWS Service Catalog

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Service Catalog](https://aws.amazon.com/servicecatalog/faqs/)

* **Exam Tips:**
  * There's a requirement for a enduser to deploy products that they don't have permissions to do otherwise, in a self-service way.
  * Used to tag provisioned resources with corresponding unique identifiers for portfolio, product, and users.
  *** How it works:**
    * 1) Admins define products and portfolios using CloudFormation Templates and Service Catalog configuration
    * 2) Deploy portfolio to any service enabled regions.
    * 3) Service Catalog users review portfolios they have permissions on and launch product(s) into service enabled regions.
    * 4) Service Catalog launchers the infrastructure using defined templates. Service catalog users don't need infrastructure permissions .. only launch permissions.
    * 5) Products are available for usage.

If you want to give your enduser permission to launch a product you need this policy created and attached.

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
