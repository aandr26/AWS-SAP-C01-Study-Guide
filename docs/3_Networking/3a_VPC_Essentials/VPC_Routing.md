# VPC Routing

* [Return to table of contents](../../../README.md)

* **Exam Tips:**
  * A subnet can only be associated with one route table.
  * Additional routes tables can be created in VPCs and associated with subnets.
  * The higher the prefix, the higher the priority of the route.
  * Route tables are created on a per vpc basis.
  * The MAIN RT is the implicit and default route table for subnets.
  * Priority of Routes:
    * (1.) Longest prefix wins
      * More specific routes always win
    * (2.) Static routes
    * (3.) Propagated routes
