---
title: "Week 4 Worklog"
date: 2026-07-13
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:
- Integrate Amazon Bedrock generative AI services to power the dynamic AI Storyteller system.
- Develop a modular `PromptBuilder` combining character profile, active inventory, and story histories.
- Design strict JSON response schemas for the AI models and code parser utilities on C# backend.

### Tasks Carried Out:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | Request and enable access to LLM models (Amazon Nova / Anthropic Claude) via Amazon Bedrock Console | 13/07/2026 | 13/07/2026 | Amazon Bedrock User Guide |
| Tue | Establish connectivity using C# AWS SDK Bedrock Runtime client and invoke models | 14/07/2026 | 14/07/2026 | AWS SDK for .NET - Bedrock |
| Wed | Write PromptBuilder logic compiling character metadata and previous action contexts into prompt payloads | 15/07/2026 | 15/07/2026 | Prompt Engineering Guide |
| Thu | Design structured JSON instructions to enforce AI outputs containing story narration, choices, and boss stats | 16/07/2026 | 16/07/2026 | Bedrock JSON Schema Setup |
| Fri | Code the JSON Parser to map raw model responses to backend C# DTOs safely | 17/07/2026 | 17/07/2026 | C# System.Text.Json Guide |
| Sat | Conduct integration testing on Bedrock invocations to measure latency, cost, and parsing reliability | 18/07/2026 | 18/07/2026 | Bedrock API Reference |

### Achievements:
- Successfully integrated .NET backend with Amazon Bedrock API using `amazon.nova-pro-v1:0` model.
- Completed a dynamic prompt generator engine injecting current player stats, items, and choices.
- Solved model output parsing by leveraging strict system guidelines, returning structured JSON containing narrative descriptions, choice nodes, and combat statistics.
