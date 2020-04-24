# AWS GuardDuty

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [What is GuardDuty](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html)

* **Exam Tips:**
  * Basically just need to know that it exists and possible use case.
  * Need to know terms:
    * Accounts - Master accounts and members.
      * Cannot be both master and member.
      * Only be member of one GuardDuty master.
    * Trust IP list
      * Can do a trusted IP list - IPs that don't generate findings.
      * Single list per-region per-account.
    * Threat list:
      * Explicitly define know malicious IPs.
      * 6 lists per-region per-account.
  * Can monitor:
    * CloudTrails
    * Route 53
    * VPC FlowLogs
  * Does require service role permissions.
  