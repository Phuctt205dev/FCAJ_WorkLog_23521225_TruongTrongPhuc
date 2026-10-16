---
title: "Week 3 Worklog"
date: 2026-10-16
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Add role selection and administrator login, session management, and logout flows.
* Complete the event management interface, coordinate API integration, and agree on rules that protect registration data.
* Check functionality, responsive layouts, and integration results locally; update project documentation.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Tuesday | - Analyze the Participant and Administrator flows; identify actions that require authentication and permission checks.<br>- Agree on event form fields, registration controls, blocking deletion when places are occupied, and preventing capacity from falling below occupied places.<br>- Design the role selection page, login page, and administration layout using the existing design system. | 13 Oct 2026 | 13 Oct 2026 | [OWASP – Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html); [Schema.org – Event](https://schema.org/Event) |
| Thursday | - Complete the interface for listing, searching, creating, and editing events, confirming deletion, and opening/closing registration.<br>- Integrate login, session checks, and logout; configure frontend API calls through the Vite proxy and handle loading states and errors.<br>- Coordinate with the backend developer on the API contract, authorization, session protection, and conflicts when updating or deleting events. | 15 Oct 2026 | 15 Oct 2026 | [OWASP – Session Management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html); [OWASP – CSRF Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html); [OWASP – Authentication](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html) |
| Friday | - Check role selection, login/reload/logout, event management, and the participant registration flow locally.<br>- Review responsive layouts, event content rendering, and cases involving insufficient permissions, data conflicts, and blocked deletion when places are occupied.<br>- Review recorded test and build/lint results; update documentation and try the local environment again to verify the outcome. | 16 Oct 2026 | 16 Oct 2026 | [AWS SAM – Validate](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/sam-cli-command-reference-sam-validate.html); [Python – unittest](https://docs.python.org/3/library/unittest.html); [Vite – Build](https://vite.dev/guide/build.html) |

### Week 3 Achievements:

* Added role selection, login, and event management screens for administrators while preserving the participant flow for browsing, searching, and registering without an account.
* Completed the interface for listing, searching, creating, editing, and deleting events, as well as opening and closing registration. The administration form supports the event name, category, time in the Vietnam time zone, location, organizer, capacity, and content, while remaining consistent with the existing design.
* Coordinated frontend integration with the administration APIs and updated the API contract to version 2. Login sessions survive page reloads and are revoked on logout; selecting a role in the interface does not grant administrator permissions.
* Learned how the frontend and backend work together to enforce permissions, protect sessions with HttpOnly/SameSite cookies, and perform CSRF/Origin checks. Rules that block deletion when places are occupied, preserve occupied places, and detect version conflicts were checked during the upgrade.
* The upgrade worklog records shared test results of 45 passing unit tests and 2 passing integration tests. Last-place contention, duplicate emails, access permissions, session management, and concurrent updates were checked.
* Frontend build/lint and SAM build/validation passed; two existing Fast Refresh warnings remain in Button and Badge. Edge headless checks covered the main flows, and the new pages showed no horizontal overflow at widths of 320, 375, 414, 768, and 1280 px. Test script content was displayed as text without execution.
* Updated local setup documentation, the API contract, the data model, and security rules. Tried the application again with an administrator account, checked backend readiness, and clarified the difference between simulated occupied places in seed data and actual registration records.

End-of-week status: Completed the role selection and event administration upgrade locally. The application infrastructure has not been deployed on AWS; production administrator provisioning options remain at the discussion stage.
