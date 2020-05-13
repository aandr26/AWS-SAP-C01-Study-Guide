# OpsWorks Architecture

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [AWS OpsWorks for Puppet Enterprise](https://docs.aws.amazon.com/opsworks/latest/userguide/welcome_opspup.html)
  * [AWS OpsWorks for Chef Automate](https://docs.aws.amazon.com/opsworks/latest/userguide/welcome_opscm.html)
  * [Using Auto Healing to Replace Failed Instances](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-autohealing.html)
  * [Managing AWS OpsWorks Stacks User Permissions](https://docs.aws.amazon.com/opsworks/latest/userguide/opsworks-security-users.html)
  * [Recipes](https://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook-installingcustom-components-recipes.html)
  * [Stacks](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks.html)
  * [Layers](https://docs.aws.amazon.com/opsworks/latest/userguide/workinglayers.html)
  * [Instances](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances.html)
  * [Apps](https://docs.aws.amazon.com/opsworks/latest/userguide/workingapps.html)

* **Exam Tips:**
  * Global service, but you can choose the region to deploy into.
  * **Stacks:**
    * Top level construct
    * Type (Dev, Prod) or function (Finance, Management) of a system.
    * Can run custom chef cookbooks but need to point it at a repository.
    * Uses instance roles for the instances it creates.
  * **Layers:**
    * OpsWorks
    * ECS
    * RDS
    * Layer is where recipies are applied.
  * **Instances:**
    * 24/7 - Base usage.
    * Time - Known periods of usage.
    * Loadbased - Everything else.
  