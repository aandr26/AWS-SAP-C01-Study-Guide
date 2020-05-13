# Elastic Beanstalk Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Adding a Database to Your Elastic Beanstalk Environment](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.managing.db.html)
  * [Using Elastic Beanstalk with Amazon Relational Database Service](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/AWSHowTo.RDS.html)
  * [Advanced Environment Customization with Configuration Files (.ebextensions)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/ebextensions.html)
  * [Environment Manifest (env.yaml)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/environment-cfg-manifest.html)

* **Exam Tips:**
  * Platform as a Service (PaaS)
  * Be aware of the platforms supported in environments.
  * **Application:**
    * Container of environments, versions, environment configurations.
    * An application can have Web Server or Worker environments.
    * Application can have multiple environments.
  * URL swapping allow for Blue/Green deployments.
  * Can save the configuration of an environment.
