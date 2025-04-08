# DevOps Support Engineer Interview Questions & Answers

## General DevOps

**Q1: What is DevOps?**  
**A:** DevOps is a set of practices that combines software development and IT operations to shorten the development lifecycle and provide continuous delivery with high quality. It emphasizes automation, collaboration, and monitoring.

**Q2: What’s the role of a DevOps Support Engineer?**  
**A:** A DevOps Support Engineer ensures smooth CI/CD pipelines, resolves build/deployment issues, manages infrastructure support, monitors system health, and assists developers with environment-related problems.

---

## CI/CD & Tools

**Q3: What CI/CD tools have you worked with?**  
**A:** Jenkins, GitHub Actions, GitLab CI/CD, CircleCI. Set up pipelines, resolved build failures, integrated tests and deployments.

**Q4: How do you troubleshoot a failed CI/CD pipeline?**  
**A:**
- Review logs for failed steps  
- Check recent code changes  
- Validate environment variables and secrets  
- Re-run with debugging enabled  
- Verify external dependencies like credentials or permissions

---

## Cloud & Infrastructure (AWS, Terraform, Kubernetes)

**Q5: What’s your experience with AWS?**  
**A:** Used services like EC2, S3, IAM, EKS, CloudWatch. Troubleshoot permission issues, monitor logs, manage instances, and support deployments.

**Q6: What is Terraform and how have you used it?**  
**A:** Terraform is an infrastructure-as-code tool. Used to provision EKS clusters, VPCs, EC2 instances, and configure remote backends with S3 and DynamoDB. Troubleshoot plan/apply errors and workspace issues.

**Q7: How do you manage Kubernetes access for users?**  
**A:** By editing the `aws-auth` ConfigMap in EKS to map IAM roles/users to Kubernetes RBAC roles.

---

## Troubleshooting & Monitoring

**Q8: What steps do you take when a production pod keeps crashing in Kubernetes?**  
**A:**
- Check pod logs: `kubectl logs <pod>`  
- Describe pod: `kubectl describe pod <pod>`  
- Look for OOM, crash loops, or misconfigurations  
- Check CPU/memory limits  
- Restart the pod or scale

**Q9: What tools do you use for monitoring and alerting?**  
**A:** Prometheus and Grafana for monitoring, CloudWatch for AWS, ELK/EFK stack for logging, PagerDuty for alerts.

---

## Security & Access

**Q10: How do you handle secrets in CI/CD?**  
**A:** Use secret managers like AWS Secrets Manager, HashiCorp Vault, or encrypted CI/CD environment variables. Never hardcode secrets.

---

## Behavioral / Real-world Scenarios

**Q11: Tell me about a time you fixed a major outage or deployment issue.**  
**A:** During a release, pods failed due to missing image tags. I quickly rolled back using Helm, fixed the tag in the pipeline, and redeployed — minimizing downtime.

**Q12: How do you prioritize support tickets or incidents?**  
**A:** I follow severity levels — production issues first. Keep stakeholders updated, document known issues, and create runbooks for recurring problems.
