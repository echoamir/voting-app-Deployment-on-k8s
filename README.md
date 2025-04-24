# Kubernetes Voting App Deployment

This project demonstrates the deployment of a full-stack voting application on a Kubernetes cluster using modern DevOps tools and best practices.

## 🧰 Cluster Provisioning

The Kubernetes cluster was provisioned using **[Kubespray](https://github.com/kubernetes-sigs/kubespray)**, providing a highly configurable and production-ready environment.

## 🔐 TLS Certificates

TLS certificates for services exposed externally are managed via **[cert-manager](https://cert-manager.io/)**, using **Let's Encrypt** as the certificate issuer.

## 📦 Application Architecture

The deployed application is a **Voting App** that includes the following components:

- `vote` (frontend)
- `result` (frontend)
- `worker` (backend processor)
- `Redis` for message queuing
- `PostgreSQL` in **high availability (HA)** mode for data persistence

All services are containerized and deployed via **Helm charts**.

## 🔄 Continuous Integration

Continuous integration pipelines are defined using **GitLab CI/CD** to automate:

- Docker image builds and pushes
- Helm chart packaging and deployment
- Linting and validation of Kubernetes manifests

## 📊 Monitoring & Observability

Monitoring is handled by:

- **Prometheus** for metrics collection
- **Grafana** for visualization and dashboards

A **federated Prometheus setup** is used to ensure metric persistence and scalability across clusters or environments.

## ⚙️ Highlights

- Production-ready Kubernetes setup with Kubespray
- Secure TLS management using cert-manager and Let's Encrypt
- Redis and PostgreSQL deployed in HA mode
- Automated GitLab CI/CD pipelines
- Scalable monitoring with Prometheus Federation
- Real-time visualization through Grafana

## 🗂 Repository Structure


