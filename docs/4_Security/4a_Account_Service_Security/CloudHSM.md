# AWS CloudHSM

* [Return to table of contents](../../../README.md)

* Useful Links:
  * [Initialize the Cluster](https://docs.aws.amazon.com/cloudhsm/latest/userguide/initialize-cluster.html)

* **Exam Tips:**
  * Behind the scenes it uses Hardware Security Module (HSM)
    * A true "single tenant" HSM
    * AWS provisioned but fully customer managed.
  * Be mindful of requirements for, CloudHSM supports them:
    * If the solution requires these services, you cannot use KMS!
      * PKCS #11
      * Java Cryptography Extensions (JCE)
      * Microsoft CyrptoNG (CNG)
    * FIPS 140-2 compliant up to level 3.
  * If it requires physical access, CloudHSM is not the right choice.
  * Better performance.
