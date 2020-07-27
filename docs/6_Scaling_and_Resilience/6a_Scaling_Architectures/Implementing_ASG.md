# Implementing Auto Scaling Groups (ASGs)

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Termination Policies](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html)

* **Exam Tips:**
  * **Deployment Types - Image baking vs Bootstraping:**
    * A flexible deployment of EC2? AMI baking is not the way to go.
    * Need to deploy something at a certain speed?
      * If using bootstrapping, additional processing time is added.
      * Gain flexibility but lose speed.
  * **Autoscaling Groups:**
    * Know the dividing line between launch configurations and ASG.
    * **ASG:**
      * Where and when to deploy instances.
      * MIN, MAX, Desired.
      * Has built-in health check.
    * **Launch configuration (Legacy):**
      * What to deploy:
        * Instance type.
        * AMI
        * Specify on-demand or spot.
        * Can enable detailed monitoring.
        * Security groups.
        * Key pairs.
      * Immutable, can create but not edit!
      * Any changes require a new launch configuration and then change the association in the ASG.
    * **Launch templates:**
      * Very similar to launch configuration.
      * Allow template versioning.
  * **Multi-AZ Implementations:**
    * Be sure to plan placement based on requirements.
    * Understand nominal instances required.
    * May not be able to accept lost availability zones.
    * Make sure you can cope with a failure by using the least amount of buffer infrastructure.
