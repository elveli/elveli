# Projects

Hands-on projects in **Kubernetes**, **AWS**, **Terraform**, **CI/CD**, and **MLOps**. Most are cost-optimized demos and labs — Spot instances, scale-to-zero node groups, one-command teardown — built to be spun up, explored, and destroyed without leaving anything running.

## Featured

| Repo | What it is |
|---|---|
| [kind-commerce-debug-lab](https://github.com/elveli/kind-commerce-debug-lab) | A tiny commerce stack ("KindKart") on a local KIND cluster with a Grafana + Loki + Promtail logging stack. It deploys healthy, then a bundled fault injector breaks it one scenario at a time — six faults covering DNS, endpoints, ports, probes, memory limits, and rollouts — and you diagnose each with Grafana logs, `kubectl`, and `k9s`. No cloud account required, just Docker and a laptop. |
| [eks-event-driven-autoscaling](https://github.com/elveli/eks-event-driven-autoscaling) | An async job-processing pipeline on EKS where autoscaling is the visible product: jobs land in SQS, KEDA scales worker pods from zero, and Karpenter provisions EC2 capacity when pods don't fit, consolidating it away once idle. Includes IRSA pod identity, an ALB ingress, Argo CD GitOps, and a GitHub Actions + OIDC + Trivy pipeline with no stored AWS keys. |
| [eks-airflow-kubeflow-demo](https://github.com/elveli/eks-airflow-kubeflow-demo) | Apache Airflow (KubernetesExecutor) orchestrating a Kubeflow Pipelines scikit-learn training run end-to-end on EKS, provisioned with Terraform, with artifacts and logs in S3 via IRSA. Tuned for minimum burn rate: Spot nodes, no NAT gateway, a scale-from-zero ML node group, and a kill switch that scales the whole cluster to zero nodes. |
| [AWS-VPC-Lattice](https://github.com/elveli/AWS-VPC-Lattice) | An interactive React simulator for AWS VPC Lattice — multi-account/multi-VPC service networking, SigV4 IAM authorization, and weighted canary routing — paired with a genuinely `terraform apply`-able 2-account stack (EC2 + Lambda targets, cross-account RAM sharing) you can actually `curl` against, not just read about. |

## Kubernetes & EKS

- [eks-troubleshooting-lab](https://github.com/elveli/eks-troubleshooting-lab) — EKS troubleshooting lab with Kubernetes manifests and Terraform for reproducing common cluster and workload issues.
- [EKS-cluster-with-Istio-and-Envoy](https://github.com/elveli/EKS-cluster-with-Istio-and-Envoy) — Terraform for an EKS cluster plus instructions to deploy Istio (Envoy under the hood) and a sample application showing traffic routing, observability, and security.
- [Crossplane-AWS-Demo](https://github.com/elveli/Crossplane-AWS-Demo) — Crossplane on AWS: Terraform provisions the EKS cluster, Helm installs Crossplane, and Crossplane manifests then provision AWS resources directly from Kubernetes.
- [cool-simple-eks](https://github.com/elveli/cool-simple-eks) — A simple EKS cluster on Spot EC2 instances (or ECS Fargate Spot) in Terraform, with Kubernetes manifests deployed via Helm.
- [Kubernetes-HPA-AWS-Demo](https://github.com/elveli/Kubernetes-HPA-AWS-Demo) — Kubernetes Horizontal Pod Autoscaler demo on AWS.
- [KubeVibe](https://github.com/elveli/KubeVibe) — A lightweight, AI-powered Kubernetes dashboard and DevOps assistant, built with React and packaged as a Helm chart for Minikube.
- [Kubernetes-on-Docker-macOS-Guide](https://github.com/elveli/Kubernetes-on-Docker-macOS-Guide) — A guide to setting up a multi-node Kubernetes cluster on macOS using Docker Desktop and Kind, as an alternative to Vagrant-based multi-node setups.

## CI/CD & GitOps

- [Tekton-AWS-Pipeline-Showcase](https://github.com/elveli/Tekton-AWS-Pipeline-Showcase) — Interactive dashboard demonstrating Tekton pipeline architecture on AWS EKS with ECR integration.
- [terraform-ecs-github-actions](https://github.com/elveli/terraform-ecs-github-actions) — Automated deployment of an AWS ECS Fargate Spot cluster and service using Terraform and GitHub Actions.
- [aws-compute-simulator](https://github.com/elveli/aws-compute-simulator) — Interactive React dashboard comparing Karpenter (EKS) and Fargate (ECS) compute strategies, orchestrated with Kargo multi-stage GitOps.
- [Kargo-ArgoCD-on-Minikube](https://github.com/elveli/Kargo-ArgoCD-on-Minikube) — Installer for Kargo and Argo CD on Minikube.
- [Ansible-Hub](https://github.com/elveli/Ansible-Hub) — Ansible automation dashboard for running and monitoring playbooks on AWS.

## Serverless & AWS Architecture

- [Docker-on-Lambda](https://github.com/elveli/Docker-on-Lambda) — Step-by-step guide and infrastructure-as-code setup for running Docker containers on AWS Lambda, pulling images from Amazon ECR.
- [aws-lambda-analytics](https://github.com/elveli/aws-lambda-analytics) — Serverless event-processing architecture on AWS Lambda using Python, DynamoDB, and SQS, with a focus on production-grade configuration.
- [Docker-AWS-ECS-Masterclass](https://github.com/elveli/Docker-AWS-ECS-Masterclass) — Interactive tutorial and showcase covering Docker image optimization and AWS Fargate deployment.
- [AWS-Static-Cloud-Showcase](https://github.com/elveli/AWS-Static-Cloud-Showcase) — A React web application with Terraform IaC and GitHub Actions CI/CD, deployed to S3 + CloudFront.
- [aws-steps-functions-demo](https://github.com/elveli/aws-steps-functions-demo) — AWS Step Functions demo provisioned with Terraform.
- [AWS-Kinesis-Demo](https://github.com/elveli/AWS-Kinesis-Demo) — A simple, low-cost AWS Kinesis demo with a producer and consumer in Python.
- [kafka-demo](https://github.com/elveli/kafka-demo) — A simple Kafka demo on AWS.
- [no-cost-multi-tier-aws](https://github.com/elveli/no-cost-multi-tier-aws) — Multi-tier AWS infrastructure in Terraform, at no or minimal cost.

## MLOps & AI

- [Agentic-Data-Analyzer](https://github.com/elveli/Agentic-Data-Analyzer) — Multi-step AI agent pipeline (parse, embed with pgvector, detect anomalies, report) powered by Gemini, deployed low-cost on AWS via Terraform.
- [MLOps-Showcase-DVC-MLflow-on-AWS](https://github.com/elveli/MLOps-Showcase-DVC-MLflow-on-AWS) — Boilerplate and documentation for setting up DVC and MLflow with AWS S3 storage provisioned via Terraform.
- [AWS-Bedrock-Agent-Builder](https://github.com/elveli/AWS-Bedrock-Agent-Builder) — AWS Bedrock agent builder with Terraform.
- [AWS-Infra-MCP-Showcase](https://github.com/elveli/AWS-Infra-MCP-Showcase) — A Model Context Protocol (MCP) dashboard for real-time serverless Terraform management and audit trailing on AWS.
- [Personal-AI-agent](https://github.com/elveli/Personal-AI-agent) — A personal AI agent that runs on a laptop or on AWS serverless.

## Observability & Ops Utilities

- [AWS-Budget](https://github.com/elveli/AWS-Budget) — Monitors AWS account spend and sends a notification when it goes over a set limit.
- [AWS-Key-Rotator](https://github.com/elveli/AWS-Key-Rotator) — AWS access key rotation utility in Python.
- [RDS-Proxy-Stress-Tester](https://github.com/elveli/RDS-Proxy-Stress-Tester) — Stress-testing tool for Amazon RDS Proxy.

## Web Apps

- [DaylightDelta](https://github.com/elveli/DaylightDelta) — Calculates and visualizes the days of the year when daylight lengthens or shortens the most, for any city in the world.
- [NorthPoleProximity](https://github.com/elveli/NorthPoleProximity) — Compares two cities and determines which one is further north.
