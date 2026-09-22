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


 
 
