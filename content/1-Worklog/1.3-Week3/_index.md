---
title: "Week 3 Worklog"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* **S3 Static Hosting:** Learn object storage design, public access permissions, and deploy a static website hosted on Amazon S3.
* **Relational Database (RDS):** Initialize, configure, and connect to relational database instances (MySQL/PostgreSQL) managed by Amazon RDS.
* **NoSQL Database (DynamoDB):** Explore NoSQL schema structures, primary keys (Partition Key and Sort Key), and run basic CRUD actions on Amazon DynamoDB.
* **System Monitoring (CloudWatch):** Configure metrics collection, set up custom alerts (Alarms), and monitor logs in Amazon CloudWatch.
* **Command Line Operations (AWS CLI):** Install, securely configure credentials, and run administration commands directly via terminal.

### Tasks to be carried out this week:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Create S3 bucket, configure bucket policy and CORS settings <br> - Deploy static HTML/CSS files for website hosting | 06/07/2026 | 06/07/2026 | Amazon S3 Static Hosting Guide |
| 2 | - Launch an Amazon RDS instance (MySQL or PostgreSQL) <br> - Set up a VPC security group and verify connectivity via DBeaver/pgAdmin | 07/07/2026 | 07/07/2026 | Amazon RDS User Guide |
| 3 | - Create a DynamoDB table with defined Partition Key and Sort Key <br> - Perform CRUD operations via AWS Console and programmatically | 08/07/2026 | 08/07/2026 | Amazon DynamoDB Developer Guide |
| 4 | - Explore CloudWatch metrics dashboard <br> - Set up an alarm to trigger an SNS email alert when an RDS metric exceeds limit | 09/07/2026 | 09/07/2026 | Amazon CloudWatch User Guide |
| 5 | - Install AWS CLI on local workspace <br> - Configure AWS credentials using `aws configure` with IAM access keys | 10/07/2026 | 10/07/2026 | AWS CLI Getting Started |
| 6 | - Write CLI scripts to manage S3 buckets, RDS status, and query DynamoDB data from command prompt | 11/07/2026 | 11/07/2026 | AWS CLI Command Reference |

### Week 3 Achievements:

* **Static Site Deployed:** Successfully deployed a fully functional static website hosted directly on Amazon S3. Understood S3 permissions, including disabling Block Public Access and adding custom Read-Only bucket policies.
* **RDS Connection Established:** Provisioned a cloud-managed PostgreSQL database. Mastered secure access setup using Security Group inbound rules to restrict connection access to my local IP.
* **NoSQL Experience:** Understood the fundamentals of NoSQL architectures compared to relational structures. Created DynamoDB tables, set up primary keys, and performed efficient CRUD operations.
* **Resource Monitoring:** Set up operational monitoring. Configured CloudWatch Alarms to track resource usage and automatically send alerts, improving system visibility.
* **Command Line Proficiency:** Standardized developer workflow by shifting from manual console operations to terminal-based automation using AWS CLI commands (`aws s3 cp`, `aws rds describe-db-instances`, etc.).
