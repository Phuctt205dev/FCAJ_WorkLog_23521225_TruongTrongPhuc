---
title: "Week 2 Worklog"
date: 2026-10-09
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Revise the event registration platform architecture to fit the learning budget.
* Finalize the eight-week project plan and test scenarios.
* Prepare the local environment and project skeleton to begin application development.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Thursday | - Assess the costs of the container-based approach and select a serverless architecture.<br>- Define the S3, CloudFront, API Gateway, Lambda, and DynamoDB components; clarify the frontend–backend flow and the approach to concurrent registrations.<br>- Develop the eight-week plan, test scenarios, and an approach to reduce the time AWS resources remain provisioned. | 8 Oct 2026 | 8 Oct 2026 | [AWS Fargate Pricing](https://aws.amazon.com/fargate/pricing/); [Elastic Load Balancing Pricing](https://aws.amazon.com/elasticloadbalancing/pricing/); [CloudFront Documentation](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html); [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html) |
| Friday | - Finalize the setup checklist and load test limits to control request counts, test duration, and costs.<br>- Prepare development tools, the Python environment, the project structure, and the GitHub repository.<br>- Run DynamoDB Local with Docker Compose; verify reads, writes, and data persistence after restarting.<br>- Run a sample API with AWS SAM CLI, check /health, connect the sample frontend, and complete the local setup instructions. | 9 Oct 2026 | 9 Oct 2026 | [Python – venv](https://docs.python.org/3/library/venv.html); [Docker Compose](https://docs.docker.com/reference/cli/docker/compose/up/); [DynamoDB Local](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html); [AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/using-sam-cli-local-start-api.html) |

### Week 2 Achievements:

* Selected a serverless architecture suited to the learning budget: a frontend on S3 and CloudFront, an API Gateway HTTP API, processing with Lambda On-Demand, and storage in DynamoDB On-Demand. Identified Terraform for infrastructure management, CloudWatch and SNS for monitoring and alerting, and GitHub Actions with OIDC as the planned CI/CD approach.
* Clarified the frontend, API, and database request flow; defined an approach using transactions to update the counter and create the registration together, aiming to prevent registrations from exceeding event capacity. The frontend will neither access the database directly nor determine slot availability.
* Developed an eight-week project plan covering setup, local development, AWS deployment, testing, documentation, demonstrations, and resource cleanup. Prioritized development on the laptop during the early stages to control costs.
* Designed five test scenarios: competing for the last remaining places, resubmitting registration requests, traffic rising and falling, accessing administrative APIs without authorization, and deploying a faulty version before reverting to a working version. Execution approaches and evaluation criteria have been defined, but the scenarios have not yet been executed.
* Defined limits for the planned load tests: 1 to 5 requests per second, with each run lasting two minutes; the read and registration tests are expected to total approximately 600 requests, excluding preparation requests. The scripts must have time limits and stop conditions, with no automatic retries during the first measurement run; results will reflect only the tested load.
* Completed the local environment and project skeleton on Windows 11: an isolated Python environment, directory structure, GitHub repository, DynamoDB Local, a sample API, and a sample frontend. Verified reads, writes, data persistence after restarting, the /health API, and frontend–backend connectivity; completed the local setup instructions.

End-of-week status: The local environment and project skeleton are ready. Event registration business features are not yet complete; system tests remain at the planning stage; the application infrastructure has not yet been deployed on AWS.

Next step: Build the frontend with sample data according to project week 2, preparing for backend development and local integration.
