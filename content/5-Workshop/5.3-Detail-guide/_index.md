---
title : "Detailed Deployment Guide"
date : 2026-08-12
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Step-by-Step Infrastructure & Backend Deployment

Follow these detailed steps to compile the monorepo shared libraries, build the .NET 8 Lambda functions, and deploy the entire serverless infrastructure using AWS CDK (C#).

---

#### Step 1: Clone Repository & Build Shared Assets

1. Navigate to the workspace directory:
   ```bash
   cd AI-Dungeon-RPG-Adventure-Game
   ```

2. Build the shared C# class library (`GameShared`):
   ```bash
   dotnet build shared/GameShared.csproj -c Release
   ```
   *Note: This automatically syncs `GameShared.dll` into `Assets/Plugins/` for Unity Client usage.*

---

#### Step 2: Build & Publish .NET 8 Lambda Backend

1. Navigate to the backend project folder:
   ```bash
   cd backend/src/GameBackend.Api
   ```

2. Restore dependencies and publish the Lambda package:
   ```bash
   dotnet lambda package --configuration Release --output-package bin/Release/net8.0/deploy-package.zip
   ```

---

#### Step 3: Bootstrap AWS CDK & Synthesize Stack

1. Navigate to the infrastructure folder:
   ```bash
   cd infrastructure
   ```

2. Bootstrap your target AWS environment (only required once per region/account):
   ```bash
   cdk bootstrap aws://<YOUR_ACCOUNT_ID>/<YOUR_REGION>
   ```

3. Synthesize CloudFormation templates:
   ```bash
   cdk synth
   ```

---

#### Step 4: Deploy Infrastructure Stack

1. Execute the CDK deployment command:
   ```bash
   cdk deploy --all
   ```

2. Once deployment completes, AWS CDK will output key resources in your terminal:
   - `CognitoUserPoolId` (e.g., `us-east-1_xxxxx`)
   - `CognitoAppClientId` (e.g., `1h2j3k4l5m6n7o8p...`)
   - `ApiGatewayUrl` (e.g., `https://xxxxxx.execute-api.us-east-1.amazonaws.com/prod/`)

3. Save these outputs to configure your Unity Client (`Assets/Resources/GameConfig.json`) or API testing tools (Postman/Insomnia).