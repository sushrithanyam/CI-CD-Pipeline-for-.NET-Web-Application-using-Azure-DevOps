# CI/CD Pipeline Design

## CI Pipeline

Code Commit
   ↓
Restore Dependencies
   ↓
Build Application
   ↓
Run Unit Tests
   ↓
Publish Artifact

---

## CD Pipeline

Artifact
   ↓
Deploy to Dev Environment
   ↓
Deploy to Staging Environment
   ↓
Approval Gate
   ↓
Deploy to Production Environment
   ↓
Monitoring (Azure Monitor + App Insights)