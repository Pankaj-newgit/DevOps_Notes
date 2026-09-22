What is DevOps.

Ans:- DevOps is a culture and set of practices that 
bridges the gap between software development (Dev) and IT operations (Ops) through collaboration and automation to deliver software faster, reliably, and continuously.” 


Q:- Devlopment flow in your company

ANS:- If you ask me about the complete deployment cycle I follow, it starts with a **PR being raised by the developer** for the required code changes.

Once the PR is raised, it goes through the required **review and approval process**. After the required approval is completed, the deployment/change request is initiated and the CI/CD pipeline is triggered.

Once the pipeline starts, it picks up the approved code and performs the required **checkout and merge activities**. Then the code goes through the **build process**, followed by the required **security checks and scans**. After the security validation is successful, the pipeline performs the required **testing and validation**.

Once all these stages are successful, the required deployment artifact or Docker image is generated and pushed to the appropriate **container registry**.

From there, the deployment process starts for the target environment. The new application version is deployed to the Kubernetes environment running on AWS. During the deployment, we monitor the rollout and make sure the required pods and services are coming up properly.

After the deployment is completed, we perform **post-deployment validation**. We check the application health, pod status, logs, APIs, CPU and memory utilization, and monitoring dashboards to make sure the application is working as expected.

If everything is healthy, we complete the deployment. If we see any issue during or after deployment, we investigate it using logs and monitoring data and, depending on the impact, either fix the issue or perform a rollback to the previous stable version.

So, at a high level, the flow is:

**PR → Approval → Change/Deployment Request → Pipeline Trigger → Checkout/Merge → Build → Security → Testing → Artifact/Image → Registry → Deployment → Validation → Monitoring → Completion/Rollback.**

 
 
 Just flow in shorts
 ======================


 “Sure. It starts with a PR, then approval and change initiation. Once approved, the CI/CD pipeline is triggered. It performs checkout and merge, followed by build, security scanning and testing.
 Once all validations are successful, the artifact or Docker image is pushed to the registry and deployed to the target Kubernetes environment.
 After deployment, we perform health checks and monitor the application. If everything looks good, we complete the deployment; otherwise, we troubleshoot and roll back if required.”



 =============================================================================


 DevOps Toolchain — Category by Category
The instructor emphasized: learn one tool per category (~10 tools total) based on market demand, not company-specific tools.

Planning
============
Jira — most widely used (~70% of companies); tickets are created and allocated here.
Confluence — used alongside Jira for storing project documentation and requirements.
Azure DevOps (ADO) — growing in cloud-native environments (~10% and rising).
Service Now — used in some enterprises.

Coding / IDE
============
Visual Studio Code (VS Code) — recommended for all languages; works as a universal IDE.
Eclipse / IntelliJ — language-specific alternatives (Java-focused).
GitHub.dev — browser-based VS Code alternative for students without a laptop (not performance-optimal but functional).
AI Copilot — integrated into VS Code; will be covered in the AI session (Day 4).

Code Management
===============
Git — installed locally; used for git push, git commit, git add, etc.
GitHub — centralized remote repository; stores all code versions, commit history, and enables collaboration.
GitLab — alternative, also used for CI/CD in some companies.
Linux kernel on GitHub cited as an example of open-source code management — 19,250+ contributors, with full commit history visible.

Build
==========
Maven — primary build tool for Java-based projects (~90% of Java projects).
Python does not require a dedicated build tool because it is interpreted (no compilation step); no artifact management tool needed for Python.

Artifact Management
==============
Nexus — stores build artifacts (WAR, JAR, EXE files) with versioning; distinct from GitHub which stores source code.
JFrog Artifactory — alternative mentioned by students.

Testing / QA
============
Selenium — browser/UI automation testing; script files have .side extension.
JMeter — performance/load testing tool.
DevOps engineers integrate these test scripts into Jenkins pipelines; QA engineers' jobs are not replaced, just automated.

CI/CD (Release)
==============

Jenkins — most popular CI/CD tool (~70% market share); 2,000+ integrations with other tools; open source, free.
GitLab CI — second most popular (~10–20%).
Helm — relevant only in Kubernetes-only environments; Jenkins is the broader choice.
Harness, GitHub Actions, CircleCI — mentioned as alternatives used in some companies.

Containerization
==================
Docker — builds container images; packages application + dependencies + OS into a portable image.
Kubernetes — manages and orchestrates containers at scale (1,000s of containers); handles automation and orchestration.
Distinction: Docker = container build/ship tool; Kubernetes = container management/orchestration tool.

Infrastructure Provisioning (IaC)
=================================
Terraform — primary tool for infrastructure deployment (creating VMs, Kubernetes clusters, cloud environments).
CloudFormation — AWS-native IaC tool; less popular than Terraform across multi-cloud.
Cloud-native tools (AWS, GCP, Azure native) also exist but Terraform is the cross-cloud standard.

Configuration Management / Automation
=====================================
Ansible — used for operation automation (e.g., installing Python on 200 VMs, weekly patching, configuration management).
Ansible Tower — UI layer on top of Ansible for enterprise use.

Monitoring
============
Prometheus + Grafana — preferred for Kubernetes environments; Prometheus = metrics database, Grafana = visualization UI.
CloudWatch — preferred for AWS-only environments.
Datadog — popular commercial monitoring tool.
Splunk — primarily a logging tool; also supports alerting and monitoring; Cisco proprietary.
Dynatrace, SolarWinds, ELK Stack — additional tools mentioned by students from their companies.
Key insight: the tool matters less than understanding what to monitor and how to configure alerting.

Release vs. Deploy — Clarification
=====================================
Release: Moving code/artifacts from one environment to another (Dev → QA → Pre-Prod → Prod); creating a new version.
Deploy: The actual act of placing the application into a target environment and making it run.
These terms are often used interchangeably in practice but have distinct meanings in the SDLC pipeline.

 
