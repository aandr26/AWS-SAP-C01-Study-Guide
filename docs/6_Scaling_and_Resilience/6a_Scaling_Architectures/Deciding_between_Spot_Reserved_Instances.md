# Deciding between Spot and Reserved Instances

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [EC2 capacity reservations](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html)
  * [EC2 scheduled instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-scheduled-instances.html)
  * [Spot fleet](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html)

* **Exam Tips:**
  * **Reserved:**
    * Don't used for variable
    * For cost savigs
    * Look for scenarios where you know you'll need the capacity.
    * Think webserver.
  * **On-Demand:**
    * Should fulfill most exam scenarios.
    * Variable load where availablity is key.
  * **Spot:**
    * Shouldn't use for nominal load.
      * Price can actually exceed on-demand.
    * Think analytics.
    * Any mention of inability to tolerate interuption or business critical workload, you should *not* use spot instances.
    * Designed to fill in capacity loads.
    * Spot fleet is a collection of spot instance pools.
