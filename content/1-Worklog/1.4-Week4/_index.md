---
title: "Week 4 Worklog"
date: 2026-07-13
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* **Infrastructure as Code (IaC):** Use AWS CDK in C# (.NET 8) to define and deploy cloud infrastructure (API Gateway, AWS Lambda, DynamoDB, Amazon Cognito).
* **Shared Library Architecture:** Build a shared .NET Standard 2.1 library (`GameShared.dll`) containing data models and DTOs, and configure automation to synchronize it with the Unity Client.
* **Authentication System:** Implement registrations and logins with Amazon Cognito using Email OTP verification.
* **Session Management:** Develop a Silent Login API leveraging Cognito Refresh Tokens to keep players logged in seamlessly.

### Tasks to be carried out this week:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Initialize AWS CDK project using C# and .NET 8 <br> - Define DynamoDB tables and Cognito User Pools structures | 13/07/2026 | 13/07/2026 | AWS CDK C# Developer Guide |
| 2 | - Code CDK stacks for API Gateway integrations and AWS Lambda handler environments | 14/07/2026 | 14/07/2026 | API Gateway CDK Reference |
| 3 | - Create the `GameShared` class library project (.NET Standard 2.1) <br> - Code mutual DTOs and item schemas | 15/07/2026 | 15/07/2026 | Microsoft .NET Class Library |
| 4 | - Write the MSBuild PostBuild Event script in the backend project file to copy `GameShared.dll` to Unity client directories | 16/07/2026 | 16/07/2026 | MSBuild Reference |
| 5 | - Integrate Amazon Cognito SDK into C# Lambda <br> - Implement sign-up, sign-in, and Email OTP validation logic | 17/07/2026 | 17/07/2026 | Cognito Identity Provider SDK |
| 6 | - Develop backend API handlers for Silent Login using Refresh Token rotation <br> - Test the flow with Unity mock client | 18/07/2026 | 18/07/2026 | JWT & Token Validation Guide |

### Week 4 Achievements:

* **IaC Automations Implemented:** Successfully automated the deployment of the entire cloud stack using AWS CDK in C#. Infrastructure is now defined as C# code, reducing manual environment setup discrepancies.
* **Type Mismatch Solved:** Set up the `GameShared.dll` shared library. Implemented MSBuild compilation hooks to automatically copy built binaries to the Unity Client folder, resolving data model synchronization errors between backend and frontend.
* **Secure Authentication Flow:** Created an Amazon Cognito User Pool with custom workflows. Users can securely register and authenticate through AWS Cognito, generating valid JWT Access, ID, and Refresh tokens.
* **Cost-Efficient Verification:** Leveraged AWS Cognito's built-in email OTP verification to manage identity validation without requiring paid external SMS or telephony gateways.
* **Seamless Player Experience:** Developed a robust Silent Login REST API. The Unity Client can now restore active player sessions automatically in the background using Refresh Tokens, removing the need for credentials entry on every game launch.
