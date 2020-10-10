# AWS Certificate Manager (ACM)

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [ACM Concepts](https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html)
  * [ACM FAQs](https://aws.amazon.com/certificate-manager/faqs/)

* **Exam Tips:**
  * Certs CANNOT leave the region they are generated or imported in.
  * Need to be aware of the architect of ACM, not implementation.
  * Natively integrates.
  * Cannot use on EC2 instances.
  * For ALB with one site you must have a cert for each region.
    * E.g. An ALB in us-west-1 requires a cert in ACM us-west-1.
    * NOT cross-region.
  * CloudFront requires the cert requested in the US East (N. Virginia)
    * CloudFront is a global service and needs an ACM cert in us-east-1
  * Generate or import certificates.
  * Can automatically renew generated certs.
  * Supported AWS services only (e.g. CloudFront and ALBs, not EC2)
