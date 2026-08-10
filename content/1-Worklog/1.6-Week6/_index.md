---
title: "Week 6 Worklog"
date: 2026-07-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* **Generative AI Integration:** Connect the C# backend to Amazon Bedrock (Claude AI) to dynamically generate and evolve RPG storylines based on player interactions.
* **Performance Optimization:** Address the Unity client freeze UI lag caused by AWS Lambda cold starts.
* **Native AOT & SnapStart:** Implement Native AOT compilation for light endpoints and AWS Lambda SnapStart for compute-heavy APIs.
* **Professional Development:** Participate in the Agent Force - Deepdive event to gain cutting-edge agentic workflow insights.

### Tasks to be carried out this week:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Integrate the Amazon Bedrock SDK inside the C# Backend <br> - Code prompts instructing Claude AI to manage player branching story paths | 27/07/2026 | 27/07/2026 | Amazon Bedrock User Guide |
| 2 | - Connect user options to Bedrock API requests <br> - Parse JSON narrative responses back to the Unity UI | 28/07/2026 | 28/07/2026 | Claude Prompt Engineering |
| 3 | - Analyze Unity logs and CloudWatch logs to diagnose Lambda cold start durations causing client UI freezing | 29/07/2026 | 29/07/2026 | CloudWatch Logs Insights |
| 4 | - Apply Native AOT compiling to lightweight endpoints (Get Profile, Inventory Check) <br> - Test response latency | 30/07/2026 | 30/07/2026 | .NET Native AOT compilation |
| 5 | - Configure AWS Lambda SnapStart for complex logic APIs (Battle Logic, Bedrock narrative API) to reduce startup latency | 31/07/2026 | 31/07/2026 | AWS Lambda SnapStart Guide |
| 6 | - Attend the Agent Force - Deepdive event <br> - Participate in workshops demonstrating agentic AI solutions | 01/08/2026 | 01/08/2026 | Agent Force Event Program |

### Week 6 Achievements:

* **Dynamic AI Storyteller:** Successfully connected the backend to Amazon Bedrock (Claude model). The game now generates personalized narratives and quest lines based on choices, parsing them back to Unity dynamically.
* **Cold Starts Diagnosed:** Identified that the .NET Runtime initialization overhead was causing up to 3-5 seconds of cold start latency, resulting in temporary UI freezes on the Unity Client.
* **Native AOT Latency Reduction:** Compiled lightweight read APIs (Get Profile, Inventory Check) using Native AOT. This reduced cold start times dramatically to a mere 20-50ms range, keeping client requests extremely fast.
* **SnapStart Deployment:** Activated AWS Lambda SnapStart for compute-intensive write APIs and AI calls. This optimizes initialization speed by utilizing execution environment snapshots, preserving fast response times without additional provisioning costs.
* **Industry Insights:** Attended the Agent Force - Deepdive event, gathering insights on autonomous agents, multi-agent frameworks, and design architectures for advanced cloud integrations.
