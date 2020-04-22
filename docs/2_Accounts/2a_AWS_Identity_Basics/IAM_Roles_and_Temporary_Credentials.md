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
    * You cannot revoke or invalidate temporary access credentials.
      * They are valid until the expiration date.
  * Products and services utilize IAM roles to interact with other services.
  * Useful for cross account functionality.
  * Access resources in different accounts via the cli.
  * Policies:
    * Trust policy:
      * Used when assumed.
      * Determine who/what can assume the role.
    * Permissions policy:
      * Checked against what the role provides.
      * Determines what actions are allowed once the role is assumed.

```BASH
# To view the temporary security credentials - swap out 'role-name' with the actual name of the attached role.
curl http://169.254.169.254/latest/meta-data/iam/security-credentials/role-name
```
