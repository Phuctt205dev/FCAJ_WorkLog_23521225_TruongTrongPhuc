---
title: "Week 4 Worklog"
date: 2026-10-24
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Add participant accounts, the ticket booking flow, and My Tickets; ensure registrations follow sales opening times and prevent duplicates.
* Unify login, role-based navigation, and the application layout; extend the event and User account management interfaces.
* Review functionality and layouts locally; complete documentation for handover.
* Learn from mentors about AI in candidate interviews, building products with Kiro Crew, and AWS AI PenTesting.

### Tasks completed this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Wednesday | - Add participant signup, login, and My Tickets interfaces.<br>- Coordinate booking API integration, associate tickets with accounts, and restrict ticket access to their owners.<br>- Complete handling of sales opening times, sold-out events, and duplicate prevention when requests are retried. | 21 Oct 2026 | 21 Oct 2026 | [OWASP – Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html); [OWASP – Password Storage](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html); [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html); [AWS – Idempotent APIs](https://aws.amazon.com/builders-library/making-retries-safe-with-idempotent-APIs/) |
| Friday | - Unify the login form, session management, and navigation for User/Admin roles.<br>- Complete the sidebar, navbar, and layouts for desktop and mobile use.<br>- Add User search, editing, and deletion; coordinate ticket and capacity handling when deleting accounts or events. | 23 Oct 2026 | 23 Oct 2026 | [OWASP – Session Management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html); [OWASP – CSRF Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html); [OWASP – Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html); [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html) |
| Saturday | - Attend a mentor meeting: watch a demo of AI in candidate interviews and learn about building products with Kiro Crew and AWS AI PenTesting.<br>- Try account, booking/ticket viewing, and administration flows locally; review layouts and resolve issues found during use.<br>- Update API documentation, the data model, and handover instructions; coordinate code integration and synchronize branches. | 24 Oct 2026 | 24 Oct 2026 | Mentor presentations; supplementary reading: [Kiro – Kiro Crew](https://kiro.dev/blog/introducing-kiro-crew/); [AWS – AI PenTesting](https://aws.amazon.com/about-aws/whats-new/2026/03/aws-security-agent-ondemand-penetration/); [Git – Worktree](https://git-scm.com/docs/git-worktree) |

### Week 4 Achievements:

* Completed participant accounts with signup, login, logout, and access to booked tickets; coordinated frontend/backend integration and access permissions.
* Completed account-linked booking with sales opening time and availability checks. Added duplicate prevention and request retry handling for interrupted connections.
* Unified login and navigation for User/Admin roles. Added a collapsible sidebar and navbar, and improved layouts for desktop and mobile use.
* Extended administration with User search, editing, and deletion, and support for deleting events with registrations. Coordinated ticket cleanup and capacity restoration where needed while preserving unrelated data.
* Reviewed the main user flows locally, including access permissions and responsive layouts. Resolved interaction, notification, and data update issues found during use.
* Updated API documentation, the data model, and handover instructions; coordinated code integration and synchronized branches.
* Watched the mentors' demo of AI in candidate interviews and gained a practical perspective on applying AI to real-world problems.
* Received an introduction to building products with Kiro Crew and gained a general understanding of coordinating AI agents to support software development.
* Learned about AWS AI PenTesting and the role of AI in supporting vulnerability discovery, validation, and remediation recommendations during application security assessments.

End-of-week status: Completed the account, booking, and administration upgrade locally. Application infrastructure has not been deployed on AWS; booking does not include payment.
