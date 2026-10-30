---
title: "Week 5 Worklog"
date: 2026-10-30
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Turn the selected serverless architecture into a concrete AWS application deployment plan.
* Prepare tools and a working account, and verify application packaging on the deployment machine.
* Estimate costs, configure budget tracking, and define resource cleanup after testing.

### Tasks completed this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Wednesday | - Review the local application, identify preparations for AWS, and complete the deployment plan.<br>- Agree to deploy the application first and add monitoring and alerts later; define functional checks and resource cleanup steps.<br>- Estimate costs within the learning budget and complete the planning documentation. | 28 Oct 2026 | 28 Oct 2026 | [AWS – CloudFront with private S3](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html); [Terraform – Plan](https://developer.hashicorp.com/terraform/cli/commands/plan) |
| Friday | - Install tools, set up an IAM account with MFA, and sign in to AWS CLI.<br>- Verify frontend build and backend packaging on the deployment machine.<br>- Adjust AWS Budgets and update the environment setup guide. | 30 Oct 2026 | 30 Oct 2026 | [AWS CLI – Browser login](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sign-in.html); [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) |

### Week 5 Achievements:

* Completed the plan to move the event registration platform from local development to AWS, defining deployment steps and verification criteria. Agreed to get the application running first, then add monitoring and alerts.
* Prepared tools and a working account on the deployment machine; signed in to AWS CLI and successfully verified frontend and backend packaging. Completed the environment preparation needed to proceed with infrastructure deployment.
* Estimated costs within the learning budget and configured budget tracking and alert thresholds in AWS Budgets to support cost control during testing.
* Completed the environment setup guide and the procedure for checking functionality, saving evidence, and removing resources after testing; defined how to run a deployment trial while preserving local data.

End-of-week status: Completed planning and deployment environment preparation. Application configuration still needs adjustment and deployment permissions need verification; the application has not been deployed or load-tested on AWS.
