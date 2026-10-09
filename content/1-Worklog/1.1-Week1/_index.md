---
title: "Week 1 Worklog"
date: 2026-10-02
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives:

* Become familiar with the internship environment at the AWS office, workplace rules, and the First Cloud AI Journey (FCAJ) program.
* Explore learning resources, how to maintain a Worklog, and the structure of Workshop documentation.
* Analyze the problem and develop a Proposal for the Online Event Registration Platform on AWS, defining the initial architecture and implementation plan.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Wednesday | - Become familiar with the internship environment, workplace rules, and the FCAJ program.<br>- Review sample Worklogs, Workshops, and learning resources.<br>- Analyze the event registration problem, define the application scope, and develop a preliminary architecture.<br>- Study high availability, Application Load Balancer, Auto Scaling, and self-healing mechanisms. | 30 Sep 2026 | 30 Sep 2026 | [FCAJ](https://cloudjourney.awsstudygroup.com/); [Worklog Sample](https://workshop-sample.awsfcaj.com/1-worklog/); [Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html); [Auto Scaling Health Checks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-health-checks.html); [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) |
| Thursday | - Continue developing the Proposal; revise the architecture to separate the frontend on Vercel from the backend on AWS.<br>- Study RDS PostgreSQL, Auto Scaling limitations during traffic spikes, and the requirement to prevent registrations from exceeding event capacity.<br>- Define a cost control approach and the use of Terraform to manage the infrastructure lifecycle. | 1 Oct 2026 | 1 Oct 2026 | [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html); [Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html); [Vercel Documentation](https://vercel.com/docs/git); [Terraform Documentation](https://developer.hashicorp.com/terraform/docs); [AWS Pricing](https://aws.amazon.com/pricing/) |
| Friday | - Study monitoring, alerting, and security with CloudWatch, SNS, IAM, Systems Manager, and Secrets Manager.<br>- Research CI/CD, Blue/Green Deployment, and Rollback.<br>- Finalize the technical direction for the Proposal; develop the implementation roadmap, test scenarios, and Workshop demo flow. | 2 Oct 2026 | 2 Oct 2026 | [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html); [SNS](https://docs.aws.amazon.com/sns/latest/dg/welcome.html); [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html); [Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html); [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html); [CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html); [CodeBuild](https://docs.aws.amazon.com/codebuild/latest/userguide/welcome.html); [CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/welcome.html) |

### Week 1 Achievements:

* Gained an understanding of workplace rules, the structure of the FCAJ program, and learning resources for the internship; learned how to maintain a Worklog and organize Workshop documentation.
* Defined the Online Event Registration Platform problem and its core functionality: viewing events, registering for events, and managing events and capacity. Planned to keep the application simple to focus on AWS infrastructure and DevOps.
* Developed the Proposal and proposed architecture: a frontend on Vercel, a backend on EC2 behind an Application Load Balancer, an Auto Scaling Group, and RDS PostgreSQL. Studied deploying the application tier across multiple Availability Zones to improve availability and support self-healing.
* Identified issues to validate during implementation: Auto Scaling delays during traffic spikes and data consistency when multiple users attempt to register for the last remaining places.
* Defined a cost control approach: develop the application locally, use RDS Single-AZ for the Workshop, and use Terraform to provision and clean up infrastructure for testing or demonstrations.
* Planned to use CloudWatch and SNS for monitoring and alerting; researched IAM, Systems Manager, and Secrets Manager for security and system administration. Studied a CI/CD approach using CodePipeline, CodeBuild, and CodeDeploy, including Blue/Green Deployment and Rollback.
* Developed an implementation roadmap and test scenarios covering normal operation, traffic spikes, EC2 or application failures, concurrent registrations, new version deployments, and failed deployments; planned the corresponding demo flow.

End-of-week status: Completed the orientation, research, and planning phase; AWS infrastructure has not yet been deployed.

Next step: Build a minimum viable product (MVP) locally, then implement each component of the AWS architecture according to the roadmap.
