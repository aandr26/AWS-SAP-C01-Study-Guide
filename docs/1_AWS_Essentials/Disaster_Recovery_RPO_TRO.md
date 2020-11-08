# Disaster Recovery: RPO and RTO

* [Return to table of contents](../../README.md)

* **Exam Tips:**
  * **Recovery Point Objective (RPO):**
    * The time between when a failure occurred and the last successful (**recoverable**) copy of necessary business data.
    * Goal is to *minimize* this length of time.
    * The business will help determine this time.
  * **Recovery Time Objective (RTO):**
    * The time between occurrence of a disaster and business required systems are operational again.
  * **Improve this by decreasing restore time:**
    * Hot Spares
    * [Processes](https://docs.aws.amazon.com/wellarchitected/latest/framework/a-failure-management.html):
      * Game days
      * Run books
