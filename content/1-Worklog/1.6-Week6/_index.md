---
title: "Week 6 Worklog"
date: 2026-11-04
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Prepare the infrastructure and application for a trial AWS deployment of the event registration platform.
* Deploy the application for a trial and remove the resources after testing.
* Update the interface and explore deployment automation.

### Tasks completed this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Tuesday | - Review the architecture and prepare access permissions for deploying the application to AWS.<br>- Build the infrastructure configuration with Terraform and update the application to support AWS.<br>- Explore how GitHub Actions can automate application checks and deployment. | 3 Nov 2026 | 3 Nov 2026 | [AWS IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html); [Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-create); [GitHub Actions](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax) |
| Wednesday | - Integrate interface updates and verify that the application can be built.<br>- Deploy the application to AWS for a trial and remove the resources afterward.<br>- Add a tool to help check resources after cleanup. | 4 Nov 2026 | 4 Nov 2026 | [CloudFront and S3](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html); [API Gateway and Lambda](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html); [Terraform Destroy](https://developer.hashicorp.com/terraform/cli/commands/destroy) |

Some AWS and Terraform references in the table were reviewed after the work was completed.

### Week 6 Achievements:

* Prepared an account and access permissions for deploying the application to AWS.
* Built the infrastructure configuration with Terraform, including components for hosting the interface, processing requests, and storing data.
* Updated the application and administration tool to support AWS alongside the existing development environment.
* Updated interface colors, rounded corners, navigation, and saved display preferences. The frontend build completed successfully.
* Completed a trial deployment to AWS, removed the trial resources afterward, and added a tool to help check the remaining resources.
* Explored GitHub Actions for automated application checks and deployment in a later phase.

End-of-week status: Completed a trial deployment and removed its resources afterward. AWS functional testing, monitoring, and load testing remain to be completed.
