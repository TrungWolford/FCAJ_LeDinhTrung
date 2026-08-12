---
title: "Week 3 Worklog"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:
- Integrate secure user authentication using Amazon Cognito User Pools.
- Develop C# backend APIs for user Registration, Confirmation, Login, and Token Refresh, connecting them to Unity Client UI.
- Design a scalable game database schema for User profiles, Characters, Inventories, StorySessions, and Battles.
- Initialize Amazon DynamoDB tables and write C# Repository classes to access and persist game states.

### Tasks Carried Out:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | Create Cognito User Pools, App Clients, and configure user schema attributes | 06/07/2026 | 06/07/2026 | AWS Cognito Developer Guide |
| Tue | Write Backend C# logic for authentication APIs (Register, Confirm, Login, Refresh) | 07/07/2026 | 07/07/2026 | AWS SDK for .NET - Cognito |
| Wed | Design basic login/signup UI in Unity, handling JWT storage and automatic session refresh | 08/07/2026 | 08/07/2026 | Unity WebRequest & Auth |
| Thu | Model database entities: User, Character, Inventory, StorySession, Battle | 09/07/2026 | 09/07/2026 | DynamoDB Modeling Best Practices |
| Fri | Provision DynamoDB tables, defining Partition Keys, Sort Keys, and Global Secondary Indexes (GSIs) | 10/07/2026 | 10/07/2026 | Amazon DynamoDB Developer Guide |
| Sat | Write C# Repository classes using AWS SDK .NET to read/write real-time game data | 11/07/2026 | 11/07/2026 | AWS SDK for .NET - DynamoDB |

### Achievements:
- Configured a fully functional user directory via Amazon Cognito with email verification flow.
- Successfully built Unity Client forms that authenticate securely and retain Bearer JWT tokens.
- Structured DynamoDB schemas with Partition Keys and Sort Keys ensuring fast query latency.
- Implemented C# data access layer (Repository) executing atomic updates and conditional queries on DynamoDB.
