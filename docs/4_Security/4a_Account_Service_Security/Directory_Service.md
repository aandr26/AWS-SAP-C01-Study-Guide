# AWS Directory Service

* [Return to table of contents](../../../README.md)

* **Notes:**
  * Simple AD:
    * Users, computers, groups.
    * AWS SSO

* **Exam Tips:**
  * Need to know the patterns and anti-patterns.
  * **Microsoft AD:**
    * If applications have a specific need to use a real Windows Active Directory, Microsoft Active directory is the one to use.
    * Microsoft AD DS supports RADIUS
    * Highly-Available by default, there are always at least two, but more can be deployed.
    * Supports trusts - one-way and two-way, and forest trust with on-premises AD.
    * Can operate through a network link failure.
    * Best used if you need to have a trust relationship between your on-premises AD and AWS and more than 5000 users.
    * Native schema extensions? Microsoft AD mode.
  * **Simple AD:**
  * **AD Connector:**
    * Requires a working network connection
    * AD connector is good for proof-of-concept or fast deployment.
    * Only redirects, no local identity data in AWS
