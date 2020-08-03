# CI/CD using AWS Code*

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [appspec.yml or appspec.json Reference](https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file.html)
  * [buildspec.yml Reference](https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html)

* **Exam Tips:**
  * AWS CodePipeline Orchestrates
  * buildspec.yml = CodeBuild
  * appspec.yml[json] = CodeDeploy
  * **CodeDeploy:**
    * EC2
    * Elastic Beanstalk or AWS OpsWorks
    * CloudFormation
    * ECS or ECS (Blue/Green)
    * AWS Service Catalog or Alexa Skill Kit
    * Amazon S3

| Code | Build | Test | Deploy |
| ---- | ----- | ---- | ------ |
| Github / Bitbucket | Jenkins | Jenkins | Jenkins or other tooling |
| CodeCommit | CodeBuild | CodeBuild | CodeDeploy |
