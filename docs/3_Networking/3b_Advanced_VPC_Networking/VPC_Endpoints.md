# VPC Endpoints

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
  * Gateway endtpoints:
    * Support S3 and DynamoDB
    * Don't occupy specific subnet
    * Are highly-available.
    * Don't need DNS, they use route tables.
    * Can utilize policies, but not security groups.
    * Can restrict resources using resorce policies.
    * Cannot be extended outside the VPC.
  * Interface endpoints:
    * Support majority of AWS services.
    * Use DNS.
    * Can use private DNS to resolve to the public DNS name.
    * One interface per service, per AZ for high availbility.
    * Can be reached outside of VPC.
    * 10GiB per second.

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
