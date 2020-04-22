# IAM Overview

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [AWS IAM Documentation](https://docs.aws.amazon.com/iam/)

## Identity & Access Managment

Lets you manage identities and allocate the permissions required for different roles, groups,  users, and organizations.

* **Notes:**
  * Authentication: When an entity represents itself, IAM verifies the identity. This process results in a verified identity.
    * Two ways to interact:
      * Username and password
      * Programmatic Access: Access key and secret key.
  * Default Implicit deny - an allow statement *is required* or else all access is implicitly denied.
    * A **deny** (explicit) always overrides an **allow**.
  * Groups are not an identity - you cannot log in as a group.
  * Identity Federation is one way to get around IAM user account limits (5000 users).

* **Exam tips:**
  * Familarize yourself with the Credential Report.
  * Watch for gotcha questions about groups
    * logging in as a group - you don't.
  * Expect a question on policy variables.
