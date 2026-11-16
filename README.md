# ☁️ Cloud Portfolio

Hands-on AWS projects built while preparing for a cloud internship. Everything is provisioned with **Terraform** and deployed with **GitHub Actions**.

**Author:** BSIT (Web & Mobile Apps), 4th year · Python · JavaScript · Kotlin · Swift
**Certifications:** AWS Certified Cloud Practitioner *(in progress)*

---

## Projects

| # | Project | Stack | Status |
|---|---------|-------|--------|
| 1 | **Cloud Resume Challenge**: serverless resume site with a live visitor counter | S3, CloudFront, Lambda (Python), API Gateway, DynamoDB, Terraform, GitHub Actions (OIDC) | 🔜 Planned |
| 2 | **Containerized web app with CI/CD**: Dockerized app deployed on every push to `main` | Docker, ECR, ECS Fargate, ALB, RDS/DynamoDB, CloudWatch, Terraform | 🔜 Planned |
| 3 | **PH Typhoon/Weather Alert System**: event-driven alerts + Kotlin Android companion app | EventBridge Scheduler, Lambda, DynamoDB, SNS, API Gateway, Terraform, Kotlin | 🔜 Planned |

Each project will have its own repo with an architecture diagram, setup steps, design decisions and a cost estimate.

---

## Principles

- **Infrastructure as Code:** no click-ops in the final version; everything is reproducible with `terraform apply`.
- **Security first:** MFA on root, no long-lived access keys, GitHub OIDC → IAM roles, least-privilege policies, secrets in SSM/Secrets Manager.
- **Cost-aware:** budget alerts on, `terraform destroy` after demos, monthly cost estimates in every README.

## Progress log

| Week | Milestone |
|------|-----------|
| 1 | AWS account secured (MFA, IAM Identity Center, budgets), AWS CLI configured, this repo created |
| 2 | |
| 3 | Serverless visitor counter (DynamoDB, Lambda, API Gateway) with unit tests. CloudFront access pending AWS review. |


