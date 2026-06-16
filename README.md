# 🚀 CI/CD Pipeline for .NET Web Application using Azure DevOps

## 📌 Project Overview
This project implements a complete CI/CD pipeline for a .NET web application using Azure DevOps and Azure App Service. The pipeline automates build, testing, deployment, and monitoring across multiple environments (Dev, Staging, Production) with approval-based production deployment.

---

## 🏗️ Architecture Overview

The system follows a modern DevOps CI/CD architecture:

- Source Control: Azure Repos (Git)
- CI Pipeline: Build, Test, Publish
- CD Pipeline: Deploy to Dev → Staging → Production
- Monitoring: Azure Application Insights

---

## ☁️ Azure Architecture Diagram

                    ┌──────────────────────┐
                    │    Developer (You)   │
                    └─────────┬────────────┘
                              │
                              ▼
                    ┌──────────────────────┐
                    │   Azure Repos (Git)  │
                    └─────────┬────────────┘
                              │  Code Push
                              ▼
        ┌────────────────────────────────────────┐
        │        Azure DevOps CI Pipeline         │
        │  - Restore Dependencies                │
        │  - Build Application                   │
        │  - Run Unit Tests (xUnit)              │
        │  - Publish Artifact                    │
        └──────────────┬─────────────────────────┘
                       │
                       ▼
              ┌────────────────┐
              │   Artifact     │
              │ (drop package) │
              └──────┬─────────┘
                     │
                     ▼
     ┌─────────────────────────────────────────┐
     │        Azure DevOps CD Pipeline         │
     └──────────────┬──────────────┬───────────┘
                    │              │
                    ▼              ▼
             ┌────────────┐  ┌──────────────┐
             │    DEV     │  │   STAGING    │
             │ App Service│  │ App Service  │
             └────┬───────┘  └────┬─────────┘
                  │               │
                  └──────┬────────┘
                         ▼
                ┌──────────────────┐
                │  PRODUCTION       │
                │ (Approval Gate)   │
                └────────┬─────────┘
                         ▼
        ┌─────────────────────────────────┐
        │ Azure Application Insights      │
        │ (Monitoring + Logs + Metrics)   │
        └─────────────────────────────────┘
---

## 🔄 CI/CD Workflow

### CI Pipeline
- Restore dependencies
- Build application
- Run unit tests (xUnit)
- Publish build artifacts

### CD Pipeline
- Deploy to Dev environment
- Deploy to Staging environment
- Production deployment requires approval
- Deploy to Production environment

---

## 🌍 Environments

| Environment | Purpose | Approval |
|------------|----------|----------|
| Dev        | Development testing | No |
| Staging    | Pre-production testing | No |
| Production | Live system | Yes |

---

## ⚙️ Technologies Used

- ASP.NET Core (.NET 8)
- Azure DevOps (YAML Pipelines)
- Azure App Service
- Azure Repos (Git)
- xUnit Testing Framework
- Azure Application Insights

---

## 📊 Monitoring

Azure Application Insights provides:
- Live request tracking
- Performance monitoring
- Failure detection
- Dependency tracking

---

## 🔐 Security Features

- Azure Service Connection for secure deployment
- Approval gate for production release
- Environment-based deployment control

---

## 🚀 Final Outcome

- Fully automated CI/CD pipeline
- Multi-environment deployment strategy
- Cloud-hosted web application
- Production-grade approval workflow
- Real-time monitoring enabled

---

## 🧠 Key Learnings

- CI/CD pipeline design using Azure DevOps
- Cloud deployment using Azure App Service
- YAML-based automation
- Unit testing integration
- Application monitoring with Azure tools

---

## 👨‍💻 Author

DevOps Project – Azure CI/CD Implementation