# AWS Directory Service

* [Return to table of contents](../../../README.md)

* **Notes:**
  * Simple AD:
    * Users, computers, groups.
    * AWS SSO

* **Exam Tips:**
  * Need to know the patterns and anti-patterns.
  * **Microsoft AD:**
    * Built on Windows Server 2012 R2.
    * If applications have a specific need to use a real Windows Active Directory, Microsoft Active directory is the one to use.
    * Microsoft AD DS supports RADIUS.
    * Highly-Available by default, there are always at least two, but more can be deployed.
    * Supports trusts - one-way and two-way, and forest trust with on-premises AD.
    * Can operate through a network link failure.
    * Supports RADIUS-based MFA.
    * Best used if you need to have a trust relationship between your on-premises AD and AWS and more than 5000 users.
    * Native schema extensions? Microsoft AD mode.
  * **Simple AD:**
  * **AD Connector:**
    * A pair of directory endpoints running in AWS (ENIs in a VPC).
    * Supports directory aware AWS products.
    * Requires a working network connection.
    * AD connector is good for proof-of-concept or fast deployment.
    * Only redirects, no local identity data in AWS.
    * Use existing on-premises AD with directory compatible AWS services without any identity data in AWS.
    * Good for proof of concepts.
    * There are risks for larger deployments - failure of network connectivity will impact functionality.
