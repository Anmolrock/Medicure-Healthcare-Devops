# Medicure - Healthcare DevOps Project

This project showcases a complete CI/CD pipeline for a **healthcare microservice application**, developed as part of a DevOps certification. It automates the entire software delivery process using modern DevOps tools like Jenkins, Docker, Kubernetes, Helm, Prometheus, and Grafana.

---

## 🏥 Project Overview

**Medicure** is a chain of super-specialty hospitals aiming to manage patient and doctor data across cities. This microservice exposes REST APIs to register, update, search, and delete doctor details using Spring Boot and an in-memory H2 database.

---

## 📦 Features

- **Microservice Architecture** (Spring Boot, Maven)
- REST APIs for doctor data
- Unit testing using **JUnit**
- HTML reports via **TestNG**
- Containerization with **Docker**
- CI/CD with **Jenkins**
- Kubernetes deployment with **Helm**
- Monitoring using **Prometheus + Grafana**
- Infrastructure automation using **Terraform** and **Ansible**

---

## 🚀 CI/CD Flow

1. Developer pushes code to GitHub (main branch)
2. Jenkins pipeline gets triggered:
    - Checkout
    - Build & Test
    - Docker Image Build & Push
    - Kubernetes Cluster Provisioning
    - App Deployment using Helm
    - Monitoring enabled
3. Auto-promotion to **production** if tests pass

---

## 🧪 REST Endpoints

| Endpoint | Method | Description |
|---------|--------|-------------|
| `/registerDoctor` | POST | Register new doctor |
| `/updateDoctor/{doctorRegNo}` | PUT | Update doctor info |
| `/searchDoctor/{doctorName}` | GET | Search doctor by name |
| `/deletePolicy/{doctorRegNo}` | DELETE | Delete doctor record |

> **Note:** Preloaded H2 data and sample requests available in `src/main/resources`.

---

## 🛠️ Tools & Tech Stack

| Category | Tools |
|---------|--------|
| Language | Java (Spring Boot) |
| Build Tool | Maven |
| Version Control | Git + GitHub |
| CI/CD | Jenkins |
| Containerization | Docker |
| Orchestration | Kubernetes (Minikube / GKE / EKS) |
| Packaging | Helm |
| Monitoring | Prometheus + Grafana |
| Infra Provisioning | Terraform |
| Configuration | Ansible |

---

## 📁 Folder Structure

medicure-healthcare-devops/
├── src/ # Spring Boot code
├── test/ # JUnit and TestNG tests
├── Jenkinsfile
├── Dockerfile
├── helm/ # Helm charts
├── k8s-manifests/ # Kubernetes YAMLs
├── terraform/ # Infra-as-Code scripts
├── monitoring/ # Prometheus/Grafana configs
├── README.md
└── project-report.pdf


---

## 📷 Monitoring Dashboard

Prometheus scrapes metrics from the app, and Grafana displays visualizations for:
- Pod health
- Cluster CPU/memory
- App latency & errors

---

## 📎 Reference

Base project idea & problem statement:  
👉 [StarAgile Healthcare Project Guide](https://github.com/StarAgileDevOpsTraining/star-agile-health-care)

---

## 📬 Author

**Anmol Upadhyay**  
DevOps Engineer  
📧 anmolupadhayay80@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/anmolupadhyay2025)

---

## 📜 License

This project is for educational and demo purposes only.

