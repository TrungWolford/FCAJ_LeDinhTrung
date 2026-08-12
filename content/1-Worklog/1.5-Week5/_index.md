---
title: "Week 5 Worklog"
date: 2026-07-20
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
- Refactor the .NET 8 backend code into granular AWS Lambda functions (Auth, Character, Inventory, Story, Battle).
- Design and configure Amazon API Gateway endpoints to securely route HTTP requests from Unity Client to Lambda handlers.
- Optimize compilation and build processes (dotnet publish) to control package sizes and minimize Lambda cold starts.

### Tasks Carried Out:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | Deconstruct core backend logic into modular code blocks: Auth, Character, Inventory, Story, Battle | 20/07/2026 | 20/07/2026 | Serverless Architecture Guide |
| Tue | Code AWS Lambda handlers in C# using Amazon Lambda SDK libraries | 21/07/2026 | 21/07/2026 | AWS Lambda .NET Programming |
| Wed | Set up Amazon API Gateway as the entry point, adding CORS configurations and Cognito Authorizers | 22/07/2026 | 22/07/2026 | AWS API Gateway Guide |
| Thu | Map API Gateway routes and bind query/body payload parameters to lambda invocation payloads | 23/07/2026 | 23/07/2026 | API Gateway Integrations |
| Fri | Execute `dotnet publish` with optimization flags to package the compiled binaries | 24/07/2026 | 24/07/2026 | .NET CLI Publish Command |
| Sat | Tune Memory limits and Timeout durations on Lambda configuration templates according to task profiles | 25/07/2026 | 25/07/2026 | Lambda Performance Tuning |

### Achievements:
- Decoupled .NET 8 project code into 5 standalone microservices hosted as AWS Lambda functions.
- Set up API Gateway serving secure HTTP endpoints validated by Cognito authorization.
- Decreased deployment package sizes utilizing release optimizations during `dotnet publish`.
- Adjusted execution parameters (RAM / Timeout thresholds) based on compute requirements, prioritizing higher budgets for Bedrock operations.
