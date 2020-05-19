# IAM Roles and Temporary Security Credentials

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * Watch for gotcha questions about roles:
    * Logging in as a role - you don't.
    * Does not have a username.
    * Does not have a password.
    * Not for one person or service.
    * No long term access credentials.
  * Revoking sessions will come up in the exam.
    * Temporary access credentials cannot be cancelled.
      * They are valid until the expiration date.
  * Products and services utilize IAM roles to interact with other services.
  * Useful for cross account functionality.
  * Access resources in different accounts via the cli.
  * **Policies:**
    * **Trust policy:**
      * Used when assumed.
      * Determine who/what can assume the role.
    * **Permissions policy:**
      * Checked against what the role provides.
      * Determines what actions are allowed once the role is assumed.
  * **STS:**
    * Generates a temporary credential ```sts:AssumeRole*```
    * They expire and don't belong to the identity.
    * Limited access
    * Used to access AWS resources
    * Request by an identity (AWS or External)
    * **A credential leak:**
      * Temp credentials cannot be invalidated on-demand - and so a specific technique needs to be used to handle credential leaks.
      * Changing the trust policy has _no_ impact on existing credentials, only on future attemps to get those credentials.
      * Changing the policy permissions will have an immediate impact on all credentials.
        * It would also impact _legitimate_ users.
      * You can add an inline deny of ```AWSRevokeOlderSessions``` which will affect any session issued before the current date and time.
    * Assume role made using the STS service which checks the role's trust policy and will then generate the necessary credentials (if the identity is in the trust policy).

```BASH
# To view the temporary security credentials - swap out 'role-name' with the actual name of the attached role.
curl http://169.254.169.254/latest/meta-data/iam/security-credentials/role-name
```
