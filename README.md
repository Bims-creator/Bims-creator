### Cloud, platform, and security engineering

Working across AWS, Azure, GCP, and Kubernetes — mostly security tooling, infrastructure-as-code, and CI/CD that doesn't fall over. The projects below are hands-on builds, not tutorials followed to the letter.

#### Security & compliance

- **[iam-lint](https://github.com/Bims-creator/iam-lint)** — static analysis for AWS IAM policies: wildcard grants, unrestricted `PassRole`, and other least-privilege violations, catchable before they reach production.
- **[aws-audit-platform](https://github.com/Bims-creator/aws-audit-platform)** — a platform-engineering pattern for AWS security auditing: a shared Python package, a self-service app scaffolder, and a release pipeline with dev → pre → prod approval gates, built around real IAM/S3 misconfiguration scanners.
- **[sanity-iam-agent](https://github.com/Bims-creator/sanity-iam-agent)** — an agent that judges whether an iam-lint finding is a real risk or a false positive, by querying a Sanity Context Knowledge Base built from iam-lint's rules paired against AWS's own documentation.

#### Multi-cloud infrastructure

- **[k8s-multicloud](https://github.com/Bims-creator/k8s-multicloud)** — one Helm chart deployed identically to GKE, EKS, and AKS, proving real multi-cloud Kubernetes portability rather than just claiming it.
- **[gcp-app-platform](https://github.com/Bims-creator/gcp-app-platform)** — a Flask app on a Compute Engine VM with private-IP Cloud SQL, provisioned via Terraform with pull-based CI/CD.
- **[gce-fleet-ops](https://github.com/Bims-creator/gce-fleet-ops)** — a cost, compliance, and exposure scanner for a GCE VM fleet; zero-cost, read-only checks.
- **[azure-landing-zone-demo](https://github.com/Bims-creator/azure-landing-zone-demo)** — Azure landing zone patterns: governance hierarchy, policy-enforced tagging, least-privilege identity, IaC in both Bicep and Terraform.
- **[cloud-infra-health-check](https://github.com/Bims-creator/cloud-infra-health-check)** — a minimal Flask health-check API with an Azure DevOps pipeline deploying to Azure App Service.

#### CI/CD & platform engineering

- **[secure-cicd-pipeline](https://github.com/Bims-creator/secure-cicd-pipeline)** — a hardened CI/CD pipeline: OIDC federation to AWS, SHA-pinned GitHub Actions, Gitleaks/CodeQL/npm audit scanning, manual approval gates.
- **[orderflow-platform](https://github.com/Bims-creator/orderflow-platform)** — an order-processing platform on Terraform-provisioned Kubernetes, ArgoCD GitOps, CI/CD with image scanning, and Prometheus/Grafana observability.
- **[security-chaos-engineering](https://github.com/Bims-creator/security-chaos-engineering)** — a custom Python fault-injection agent for chaos-testing security invariants (fail-open vs. fail-closed) on a 3-service Kubernetes app.
