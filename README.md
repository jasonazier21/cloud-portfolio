# ☁️ Cloud Portfolio

Hands-on AWS projects built while preparing for a cloud internship. Two projects are running on AWS; I'm next rebuilding them as **Terraform** and adding **GitHub Actions** deployments, and every project is designed to follow the same approach.

**Author:** BSIT (Web & Mobile Apps), 4th year · Python · JavaScript · Kotlin · Swift
**Certifications:**
- IT Specialist: Cloud Computing (Certiport/Pearson), *exam scheduled Nov 26, 2026*
- AWS Certified Cloud Practitioner *(planned)*

---

## Projects

| # | Project | Stack | Status |
|---|---------|-------|--------|
| 1 | **Cloud Resume Challenge**: serverless resume site with a live visitor counter. [Live site](https://jasonazier21.github.io/resume-frontend/) · [Frontend repo](https://github.com/jasonazier21/resume-frontend) · [Backend repo](https://github.com/jasonazier21/resume-backend) | **Built:** Lambda (Python) with unit tests, API Gateway HTTP API, DynamoDB, IAM least privilege, CORS. **Next:** S3 + CloudFront, Terraform, GitHub Actions (OIDC) | 🚧 In progress |
| 2 | **Containerized web app with CI/CD**: Dockerized app deployed on every push to `main` | Docker, ECR, ECS Fargate, ALB, RDS/DynamoDB, CloudWatch, Terraform | 🔜 Planned |
| 3 | **PH Typhoon/Weather Alert System**: scheduled weather checks with email alerts. [Repo](https://github.com/jasonazier21/typhoon-alert-backend) | **Built:** EventBridge Scheduler (every 30 min), Lambda (Python) with 9 unit tests, DynamoDB with TTL, SNS email alerts with cooldown, IAM least privilege. **Next:** Terraform, GitHub Actions, Kotlin Android companion app | ✅ Deployed, running |

Each project has its own repo with an architecture diagram, setup steps, design decisions and a cost estimate.

> **Hosting note:** the Project 1 front end is temporarily on GitHub Pages because my new AWS account is waiting on a review before it can create CloudFront distributions. The private S3 bucket is already prepared for the final setup.

---

## Principles

- **Infrastructure as Code:** no click-ops in the final version; everything is reproducible with `terraform apply`.
- **Security first:** MFA on root and admin users, no long-lived access keys, GitHub OIDC → IAM roles, least-privilege policies, secrets in SSM/Secrets Manager.
- **Cost-aware:** budget alerts on, `terraform destroy` after demos, monthly cost estimates in every README.

## Progress log

| Week | Milestone |
|------|-----------|
| 1 | AWS account secured (root MFA, IAM admin user with MFA, budget alerts), AWS CLI configured with short-lived `aws login` credentials, this repo created |
| 2 | Resume website built (HTML/CSS/JS) and uploaded to a private S3 bucket. CloudFront setup blocked pending AWS account verification |
| 3 | Serverless visitor counter (DynamoDB, Lambda, API Gateway) with unit tests. CloudFront access pending AWS review |
| 3+ | Resume site live over HTTPS on GitHub Pages (temporary hosting), architecture diagram and write-up added |
| 4 | PH typhoon alert system deployed: EventBridge → Lambda → Open-Meteo → DynamoDB → SNS email, tested end to end with a forced alert |
