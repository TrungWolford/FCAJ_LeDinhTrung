---
title: "Week 7 Worklog"
date: 2026-08-03
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:
- Enhance system security by migrating sensitive settings to Environment Variables and auditing IAM Roles.
- Establish system monitoring and logging using Amazon CloudWatch Dashboards and Alarms.
- Analyze and optimize cloud spend utilizing AWS Cost Explorer, removing redundant resources.

### Tasks Carried Out:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | Refactor hard-coded configurations (Client IDs, Resource Names) into Lambda Environment Variables | 03/08/2026 | 03/08/2026 | AWS Lambda Env Variables |
| Tue | Audit and restrict IAM policies for Lambda roles, implementing resource-level permissions | 04/08/2026 | 04/08/2026 | AWS IAM Policies Review |
| Wed | Set up CloudWatch Logs to collect application execution and error logs from the .NET code | 05/08/2026 | 05/08/2026 | CloudWatch Logs Guide |
| Thu | Design a custom CloudWatch Dashboard displaying system health metrics (Duration, Throttle, Error Count) | 06/08/2026 | 06/08/2026 | CloudWatch Dashboards Setup |
| Fri | Configure CloudWatch Alarms sending email notifications upon error spikes or budget overruns | 07/08/2026 | 07/08/2026 | CloudWatch Alarms Guide |
| Sat | Analyze spending trends with AWS Cost Explorer and clean up orphan resources to maintain budget | 08/08/2026 | 08/08/2026 | AWS Cost Explorer Guide |

### Achievements:
- Eliminated security vulnerabilities related to hard-coded properties by externalizing environment variables.
- Created operational visibility using centralized CloudWatch logs and graphical dashboards.
- Reduced overall cloud costs by identifying and deleting unutilized testing assets during audit sessions.
