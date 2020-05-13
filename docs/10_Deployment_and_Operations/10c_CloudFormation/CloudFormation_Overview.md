# CloudFormation Overview

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Working with AWS CloudFormation StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html)

* **Exam Tips:**
  * Stack operations create an event stream.
  * **Logical vs Physical Resources:**
    * Logical:
      * Name as defined in the resources section of a template.
    * Physical:
      * Takes logical ID and creates corresponding physical resource.
    * Templates -> Creates Stacks -> Stacks manage the created resources.
  * **Stack Roles:**
    * Stack roles allows you to grant granuler permissions to manage resources in a stack through stack operations, without giving them permissions to directly manage the resources.
    * This allows a seperation of roles: Engineer to create stacks and Jr. Engineers to update stacks.
  * **Stack Sets:**
    * Create, update, or delete stacks across multiple accounts and regions with a single operation.
  * **Custom Resources:**
    * Used to write custom provisioning objects.
