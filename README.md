**Cloud Run Serverless Deployment on GCP**

**Designed and deployed a serverless containerized application using Google Cloud Run with autoscaling, HTTPS endpoint exposure, and managed infrastructure. **
This project demonstrates modern serverless architecture, container deployment, scale-to-zero capability, and compute service trade-off analysis 
and also highlights architectural differences between Cloud Run, Compute Engine, and GKE.

# Architecture Diagram

# Services Used
| Service | Purpose |
|---|---|
| Cloud Run | Serverless container hosting |
| Artifact Registry Public Image | Sample container image |
| HTTPS Endpoint | Secure application access |
| Autoscaling | Dynamic scaling |

# Objectives

- Understand serverless architecture
- Deploy containerized applications
- Learn Cloud Run fundamentals
- Understand autoscaling behavior
- Compare Cloud Run with Compute Engine and GKE
- Practice compute service decision-making
# Architecture Flow

Users → HTTPS Endpoint → Cloud Run Service → Containerized Application

# Step-by-Step Implementation

## Step 1 — Created GCP Project

Created a new GCP project:

cloudrun-serverless-lab

Purpose:
- isolate resources
- manage billing
- maintain clean architecture environments

## Step 2 — Enabled Cloud Run API

Navigated to:

APIs & Services → Library

Enabled:

Cloud Run Admin API

Purpose:
- allow Cloud Run deployments
- enable serverless container management

## Step 3 — Opened Cloud Run Console

Navigated to:

Cloud Run → Deploy a Web Service

Purpose:
- deploy a public-facing serverless application

## Step 4 — Configured Cloud Run Service

| Setting | Value |
|---|---|
| Service Name | hello-cloudrun |
| Region | asia-south1 |
| Deployment Type | Existing Container Image |
| Authentication | Allow public access |

## Step 5 — Used Sample Container Image

Container Image:

us-docker.pkg.dev/cloudrun/container/hello

Purpose:
- deploy sample application quickly
- understand Cloud Run deployment workflow

## Step 6 — Enabled Public Access

Selected:

Allow unauthenticated invocations

Purpose:
- allow public browser access
- expose application via HTTPS endpoint

## Step 7 — Deployed Cloud Run Service

Deployment Status:
- Creating service → Completed
- Creating revision → Completed
- Routing traffic → Completed

Cloud Run automatically:
- provisioned infrastructure
- configured scaling
- generated HTTPS endpoint
- managed runtime environment

## Step 8 — Accessed Application

Generated URL:

https://hello-cloudrun-xxxxx.asia-south1.run.app

Result:
✅ Application successfully accessible through browser

# Key Learnings

| Concept | Learning |
|---|---|
| Serverless Architecture | No VM management |
| Cloud Run | Fully managed compute |
| Autoscaling | Automatic elasticity |
| Containers | Portable workloads |
| HTTPS | Built-in secure access |
| Scale-to-zero | Cost optimization |
| Managed Infrastructure | Reduced operational overhead |

# Cloud Run vs Compute Engine

| Area | Compute Engine | Cloud Run |
|---|---|---|
| Infrastructure Management | Manual | Fully Managed |
| Scaling | Manual/MIG | Automatic |
| OS Access | Full | No |
| Operational Overhead | Higher | Lower |
| Deployment Speed | Slower | Fast |
| Best Use Case | Legacy/custom apps | APIs/serverless apps |

# Cloud Run vs GKE

| Area | GKE | Cloud Run |
|---|---|---|
| Kubernetes Control | Full | Abstracted |
| Complexity | Higher | Lower |
| Operational Overhead | Medium–High | Very Low |
| Flexibility | High | Moderate |
| Best Use Case | Enterprise microservices | Fast APIs/services |

# Challenges Faced

- Understanding Cloud Run authentication options
- Differentiating public vs authenticated access
- Understanding autoscaling behavior
- Learning serverless compute architecture concepts

# Production Improvements
For enterprise-grade deployment:

- Custom domain integration
- Cloud Armor protection
- CI/CD pipeline integration
- Secret Manager integration
- IAM authentication
- Cloud Monitoring & Logging
- VPC connector for private access

- # Final Outcome

Successfully deployed and accessed a serverless containerized application using Google Cloud Run while understanding serverless architecture &
autoscaling behavior, HTTPS exposure, scale-to-zero capability, and operational trade-offs between Cloud Run, Compute Engine, and GKE.
