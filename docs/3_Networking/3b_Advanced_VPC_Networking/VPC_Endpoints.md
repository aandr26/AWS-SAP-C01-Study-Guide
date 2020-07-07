# VPC Endpoints

* [Return to table of contents](../../../README.md)

* **Notes:**
  * Two types:
    * Gateway Endpoint.
      * VPC based.
      * Highly available.
    * Interface Endpoint
      * Occupy a subnet.
      * Physical network interface is used.
  * Directing traffic through a single origination point.

* **Exam Tips:**
  * The endpoint controls restrictions.
  * Only limits access when it is being access through that endpoint.
  * **Gateway endpoints:**
    * Provide private access to S3 and DynamoDB
    * Don't occupy specific subnet
    * Are highly-available.
    * Don't need DNS, they use route tables.
    * Can utilize policies, but not security groups.
    * Can restrict resources using resorce policies.
      * Only accept operations coming from a gateway endpoint. ie S3
    * Cannot be extended outside the VPC.
    * Regional.
  * **Interface endpoints:**
    * Support majority of AWS services.
      * Anything not S3 and DynamoDB
    * Not highly available by default
      * Add one endpoint, to one subnet, per AZ used in the VPC.
    * Network access controlled via SGs
    * Also support endpoint policies - What can be done with the endpoint.
    * Use DNS.
    * Can use private DNS to resolve to the public DNS name.
    * Can be reached outside of VPC.
    * 10 GiB per second.

## Example Resource Policy

```JSON
{
    "Version": "2012-10-17",
    "Id": "Policy1415115909152",
    "Statement": [
        {
            "Sid": "Access-to-specific-VPCE-only",
            "Principal": "*",
            "Action": "s3:*",
            "Effect": "Deny",
            "Resource": [
                "arn:aws:s3:::s3bucketnamehere",
                "arn:aws:s3:::s3bucketnamehere/*"
            ],
            "Condition": {
                "StringNotEquals": {
                    "aws:sourceVpce": "vpce-idhere"
                }
            }
        }
    ]
}
```
