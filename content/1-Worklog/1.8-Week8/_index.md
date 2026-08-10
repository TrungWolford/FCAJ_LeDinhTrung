---
title: "Week 8 Worklog"
date: 2024-02-19
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Understand AWS messaging services: SQS, SNS, and SES.
* Learn about decoupled application architectures.
* Master queue-based processing and event-driven designs.
* Explore pub/sub patterns and message filtering.

### Tasks to be carried out this week:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1   | - Learn SQS fundamentals (Standard vs FIFO) <br> - Understand message visibility timeout <br> - Explore queue attributes and permissions | 30/07/2026 | 30/07/2026 | AWS SQS User Guide |
| 2   | - Create and configure SQS queues <br> - Send and receive messages using SDK <br> - Implement message processing workers | 31/07/2026 | 31/07/2026 | AWS SQS Configuration |
| 3   | - Learn SNS fundamentals and pub/sub pattern <br> - Create SNS topics and subscriptions <br> - Configure message filtering | 01/08/2026 | 01/08/2026 | AWS SNS User Guide |
| 4-5 | - Integrate SNS with SQS for fan-out pattern <br> - Set up email notifications using SES <br> - Build event-driven application | 02/08/2026 | 03/08/2026 | AWS Messaging Patterns |

### Week 8 Achievements:

* Gained comprehensive understanding of AWS messaging services for building decoupled applications.

* Learned about SQS Standard queues for high throughput and SQS FIFO for ordering guarantees.

* Successfully created SQS queues with appropriate configurations for different use cases.

* Implemented message visibility timeout to handle processing failures gracefully.

* Built message processing workers to consume and process messages from SQS queues.

* Learned about SNS as a fully managed pub/sub messaging service.

* Created SNS topics and configured multiple subscription types (SQS, Lambda, HTTP, email).

* Implemented message filtering to route specific messages to appropriate subscribers.

* Set up the SNS-to-SQS fan-out pattern for reliable message distribution.

* Configured Amazon SES for sending transactional emails.

* Built event-driven applications using SNS and SQS together.

* Implemented dead-letter queues for handling failed messages.

* Understood message ordering and delivery guarantees across messaging services.

* Monitored queue metrics and configured alarms for operational visibility.

* Created scalable, decoupled application architectures using messaging services.
  * View EC2 service
  * Create and manage key pairs
  * Check information about running services
  * ...

* Acquired the ability to connect between the web interface and CLI to manage AWS resources in parallel.
* ...
