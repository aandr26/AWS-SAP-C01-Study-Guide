# Identity Federation

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [ID Role Providers SAML](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html)
  * [ID Role Providers OIDC Cognito](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_oidc_cognito.html)

* **Exam Tips:**
  * Access console as well as cli and api:
    * Use ```AssumeRoleWithSAML```
  * **SAML 2.0:**
    * Indirectly use on-premises IDs with AWS (Console and CLI)
    * Used when using an Enterprise Identity Provider that is also SAML 2.0 compatible
    * Existing identity management team.
    * Desire single source of truth for users, and/or more than 5,000 users.
    * If a question mentions Google, Facebook, Web, etc, SAML 2.0 is not the correct option.
    * Assumes a IAM Role and used AWS Temporary Credentials which have 12 hour validity.
  * **AWS SSO:**
    * On-Prem AD (Two way trust or AD connector)
    * Preferred by AWS to SAML 2.0
    * Work place vs customer identities:
      * Customer - Web Apps, Google, Twitter - Cognito
      * Workplace - AWS SSO
    * Requires an Organization.
  * **Cognito:**
    * For customers
