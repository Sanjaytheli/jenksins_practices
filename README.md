# Jenkins

## What is Jenkins?

Jenkins is an **open-source automation server** used by developers and testers to **build, test, and deploy applications automatically**.

It helps implement:

- **Continuous Integration (CI)**
- **Continuous Delivery (CD)**
- **Continuous Deployment (CD)**

---

# How Jenkins Works

## 1. Automation Server
Jenkins runs in the background and automates repetitive tasks such as:

- Compiling source code
- Running unit tests
- Executing integration tests
- Packaging applications
- Deploying applications

Whenever developers push new code to the repository, Jenkins automatically starts the pipeline.

---

## 2. Controller and Agents

Jenkins follows a **Controller-Agent (Master-Worker)** architecture.

### Controller
The Jenkins Controller is responsible for:

- Scheduling jobs
- Managing pipelines
- Assigning work to agents
- Monitoring build status

### Agents

Agents perform the actual work such as:

- Building applications
- Running tests
- Creating Docker images
- Deploying applications

This architecture allows multiple builds to run simultaneously.

---

## 3. Plugins

Jenkins provides thousands of plugins that integrate with popular tools such as:

- Git
- GitHub
- Docker
- Kubernetes
- Maven
- Gradle
- SonarQube
- AWS
- Slack
- Jira

Plugins extend Jenkins functionality without modifying the core application.

---

# Key Benefits

## Early Bug Detection

Jenkins automatically runs tests whenever code changes are pushed.

Benefits:

- Detect bugs early
- Reduce production issues
- Improve software quality

---

## Saves Time

Jenkins automates repetitive tasks like:

- Build
- Test
- Package
- Deploy

This eliminates manual work and speeds up development.

---

## Flexibility

Jenkins supports:

### Operating Systems

- Windows
- Linux
- macOS

### Programming Languages

- Java
- Python
- Node.js
- Go
- PHP
- .NET
- C/C++

---

# How Jenkins Fits into CI/CD

When a developer writes code and pushes it to Git, Jenkins automatically performs several steps before deploying the application.

```
Developer
    │
    ▼
Write Code
    │
    ▼
Git Commit
    │
    ▼
Git Push
    │
    ▼
Git Repository (GitHub / GitLab / Bitbucket)
    │
    ▼
Jenkins Trigger
    │
    ▼
Pipeline Starts
```

---

# Jenkins Pipeline Steps

## Step 1: Source Code Checkout

Jenkins pulls the latest source code from Git.

```
Git Repository
       │
       ▼
Jenkins Checkout
```

---

## Step 2: Build

Compile the application.

Examples:

- Maven
- Gradle
- npm
- yarn

Output:

```
Source Code
      │
      ▼
Compile
      │
      ▼
Build Artifact
```

---

## Step 3: Unit Testing

Run unit tests to verify individual functions and classes.

Examples:

- JUnit
- NUnit
- Jest
- PyTest

If tests fail:

```
Build
   │
   ▼
Unit Tests
   │
   ├── Pass ✅
   └── Fail ❌ (Pipeline Stops)
```

---

## Step 4: Code Quality Scan

Analyze the code for:

- Bugs
- Vulnerabilities
- Code Smells
- Duplicate Code

Common Tool:

- SonarQube

---

## Step 5: Package

Create deployable files.

Examples:

- JAR
- WAR
- ZIP
- Docker Image

---

## Step 6: Store Artifact

Upload artifacts to repositories such as:

- Nexus
- JFrog Artifactory
- AWS S3

---

## Step 7: Deploy

Deploy the application to environments like:

- Development
- QA
- Staging
- Production

Deployment targets:

- EC2
- Kubernetes
- Docker
- Virtual Machines
- On-Prem Servers

---

## Step 8: Integration Testing

Verify communication between different modules.

Example:

```
Frontend
     │
     ▼
Backend
     │
     ▼
Database
```

---

## Step 9: Acceptance Testing

Validate the application against business requirements.

Usually performed by:

- QA Team
- Product Team

---

## Step 10: Production Deployment

Deploy the application to the live production environment.

```
Staging
    │
    ▼
Production
```

---

# Complete Jenkins CI/CD Workflow

```
Developer
     │
     ▼
Write Code
     │
     ▼
Git Commit
     │
     ▼
Git Push
     │
     ▼
GitHub/GitLab
     │
     ▼
Jenkins Trigger
     │
     ▼
Checkout Code
     │
     ▼
Build
     │
     ▼
Unit Testing
     │
     ▼
Code Quality Scan
     │
     ▼
Package
     │
     ▼
Artifact Repository
     │
     ▼
Deploy to Dev
     │
     ▼
Integration Testing
     │
     ▼
Deploy to QA
     │
     ▼
Acceptance Testing
     │
     ▼
Deploy to Production
```

---

# Popular Tools Used with Jenkins

| Purpose | Tool |
|----------|------|
| Version Control | Git, GitHub, GitLab |
| Build | Maven, Gradle, npm |
| Testing | JUnit, Jest, PyTest |
| Code Quality | SonarQube |
| Containerization | Docker |
| Orchestration | Kubernetes |
| Artifact Repository | Nexus, Artifactory |
| Cloud | AWS, Azure, GCP |
| Notifications | Slack, Email |

---

# Summary

Jenkins is a powerful automation server that helps teams automate the software development lifecycle.

It performs tasks such as:

- Source Code Checkout
- Build
- Unit Testing
- Code Quality Analysis
- Package Creation
- Artifact Storage
- Deployment
- Integration Testing
- Production Release

By automating these processes, Jenkins enables faster, more reliable, and consistent software delivery.
