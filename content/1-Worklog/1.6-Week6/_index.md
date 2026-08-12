---
title: "Week 6 Worklog"
date: 2026-07-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:
- Automate infrastructure provisioning using Infrastructure as Code (IaC) via AWS CDK with C#.
- Define programmatic constructs for Cognito User Pools, DynamoDB Tables, Lambda Functions, API Gateway, S3, and CloudWatch.
- Decouple the infrastructure codebase into separate Stacks to improve manageability and separation of concerns.
- Master CLI commands in the CDK deployment lifecycle: `cdk synth`, `cdk deploy`, and `cdk destroy`.

### Tasks Carried Out:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | Install AWS CDK CLI, initialize a C# CDK project, and study Stacks and Constructs | 27/07/2026 | 27/07/2026 | AWS CDK Getting Started |
| Tue | Code storage resources stack creating S3 Buckets and DynamoDB tables with Partition/Sort Keys | 28/07/2026 | 28/07/2026 | AWS CDK Database Construct |
| Wed | Program identity resources stack configuring Cognito User Pools and App Clients | 29/07/2026 | 29/07/2026 | AWS CDK Cognito Construct |
| Thu | Define serverless compute resources, linking Lambdas with proper IAM Roles (DynamoDB access, Bedrock invoke) | 30/07/2026 | 30/07/2026 | AWS CDK IAM & Lambda |
| Fri | Establish API Gateway stack specifying integration routes, CORS rules, and Cognito Authorizers | 31/07/2026 | 31/07/2026 | AWS CDK API Gateway |
| Sat | Practice CLI management: generate CloudFormation templates via `cdk synth`, deploy via `cdk deploy`, and clean up via `cdk destroy` | 01/08/2026 | 01/08/2026 | AWS CDK CLI Commands |

### Achievements:
- Codified the game's entire AWS architecture using C# CDK, removing the need for manual configuration.
- Structured codebases into decoupled, reusable stacks (StorageStack, IdentityStack, ComputeStack, ApiStack).
- Validated template outputs locally and executed safe deployments to AWS, gaining experience in IaC patterns.
