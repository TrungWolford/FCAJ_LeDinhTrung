---
title: "Week 2 Worklog"
date: 2026-06-29
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:
- Initialize a secure AWS environment and establish foundational security practices.
- Study Amazon S3 configuration, bucket access policies, and CORS setups.
- Get familiar with AWS CLI, Serverless core concepts, and AWS CDK (C#) IaC framework.
- Upload initial game assets to S3 buckets for the client to download.

### Tasks Carried Out:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | Enable MFA for AWS Root account to secure administrative access | 29/06/2026 | 29/06/2026 | AWS MFA Setup Guide |
| Tue | Create administrative and developer IAM users matching Least Privilege | 30/06/2026 | 30/06/2026 | AWS IAM Best Practices |
| Wed | Create S3 buckets for hosting game assets and write public access policies | 01/07/2026 | 01/07/2026 | Amazon S3 Developer Guide |
| Thu | Configure Cross-Origin Resource Sharing (CORS) rules on S3 for game client | 02/07/2026 | 02/07/2026 | Amazon S3 CORS Guide |
| Fri | Install AWS CLI locally and configure authentication credentials | 03/07/2026 | 03/07/2026 | AWS CLI User Guide |
| Sat | Study Serverless concepts, explore AWS CDK in C#, and upload game assets to S3 | 04/07/2026 | 04/07/2026 | AWS CDK Intro / Game Assets |

### Achievements:
- Root account is safely locked down with MFA. Everyday commands run under dedicated IAM users.
- Built a working S3 asset bucket with public read policies and CORS configured to allow Unity download.
- Successfully verified local AWS CLI connectivity, and gained a clear understanding of AWS CDK IaC lifecycle.
