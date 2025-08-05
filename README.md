# Medicure - Healthcare DevOps Project

This project implements a CI/CD pipeline for a healthcare microservice using modern DevOps tools.

## 🔧 Tech Stack
- Spring Boot (Microservice with H2 DB)
- Docker & Docker Hub
- Jenkins (CI/CD Pipeline)
- Kubernetes (Deployment & Scaling)
- Helm (Packaging & Release)
- Prometheus + Grafana (Monitoring)
- Ansible & Terraform (Optional - Infra/Config Mgmt)

## 📦 Features
- REST APIs for doctor registration/search/update/delete
- Jenkins pipeline with build, test, Dockerize & deploy stages
- Kubernetes manifests for automated deployments
- Monitoring dashboards for clusters and pods

## 📁 Folder Structure
_Refer to repo structure for details._

## 📌 Deployment Trigger
- Push to GitHub triggers Jenkins pipeline
- Auto CI/CD to dev/test/prod clusters
