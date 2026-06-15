# Architecture Diagram (CI/CD for .NET App)

## Flow

Developer
   |
   v
Azure Repos (Git)
   |
   v
Azure DevOps CI Pipeline
   |
   |--> Restore Dependencies
   |--> Build Application
   |--> Run Unit Tests
   |
   v
Build Artifact
   |
   v
CD Pipeline (Planned)
   |
   |--> Dev Environment
   |--> Staging Environment
   |--> Production Environment (Approval Gate)
   |
   v
Azure Monitor + Application Insights