# Patch Manager

[Return to table of contents](../../../README.md)

* **Exam Tips:**
  * **Core Components:**
    * Patch Baseline
      * Defines what should be installed
      * Predefined Patch Baselines:
        * Linux - AWS-[OS]DefaultPatchBaseline,
        * Windows - AWS-DefaultPatchBaseline - Critical and security updates
          AWS-WindowsPredefinedPatchBaseline-OS - Critical and security updates
          AWS-WindowsPredefinedPatchBaseline-OS-Applications - Critical and security updates + MS app updates
    * Patch Groups
      * Groups of resources in SSM, which resources to patch
    * Maintenance Windows
      * When to apply patches
    * Run Command
      * How patches are actually installed
    * Concurrency & Error Threshold
      * How many to patch and how many errors to tolerate before   failing.
    * Compliance
      * Is it compliant with a set of standards?
  * **Architecture:**
    * (1) Define Patch Baselines - What gets installed
    * (2) Create Patch groups - Targets for patch tasks.
    * (3) Maintenance windows - Define schedule, duration, targets and tasks.
    * (4) AWS-RunPatchBaseline runs with a baseline and targets.
    * (5) Checks for compliance using Systems Manager Inventory
