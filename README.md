# 🎬 Netflix DevSecOps Project on Google Cloud (GCP)

A full end-to-end **DevSecOps pipeline** built from scratch on **Google Cloud Platform (GCP)** — deploying a Netflix-style Node.js application with complete CI/CD, security scanning, container orchestration, and monitoring. ☁️🚀  

This project helped me deeply understand how real-world DevSecOps workflows actually connect, break, and finally work together!

---

## 🧩 Project Overview

The goal of this project was to implement a **secure, automated CI/CD pipeline** using modern DevOps and Security tools — and deploy a Netflix-style web app on **Google Kubernetes Engine (GKE)**.

Most tutorials use AWS, so I challenged myself to recreate the entire setup on **GCP** using Compute Engine, GKE, and GCR.

---

## ⚙️ Tech Stack & Tools

| Category | Tools Used |
|-----------|-------------|
| **CI/CD** | Jenkins |
| **Code Quality & Security** | SonarQube, OWASP Dependency Check, Trivy |
| **Containerization** | Docker |
| **Container Registry** | Google Container Registry (GCR) |
| **Orchestration** | Kubernetes (GKE) |
| **Continuous Deployment** | ArgoCD |
| **Monitoring & Alerting** | Prometheus, Grafana |
| **Application** | Node.js (Netflix-style web app) |
| **Cloud Platform** | Google Cloud Platform (GCP) |

---

## 🧠 Architecture Flow

Developer → GitHub → Jenkins → SonarQube + OWASP + Trivy → Docker Build & Push → GCR → ArgoCD → GKE Deployment → Prometheus & Grafana Monitoring

markdown
Copy code

---

## 🚀 Key Highlights

- ✅ Built Jenkins pipeline with automated build, test, and deployment stages  
- ✅ Integrated **SonarQube**, **OWASP**, and **Trivy** for static and dependency scans  
- ✅ Containerized the app using **multi-stage Docker builds**  
- ✅ Deployed microservices to **Google Kubernetes Engine (GKE)**  
- ✅ Configured **Prometheus** and **Grafana** dashboards for Jenkins & cluster metrics  
- ✅ Implemented **GitOps** deployment using **ArgoCD**  
- ✅ Fixed Node.js dependency issues and YAML configuration errors manually  

---

## 🏗️ Project Setup (High-Level)

### 1. Infrastructure Setup
- Created Compute Engine VMs for Jenkins, SonarQube, Prometheus, Grafana, and ArgoCD.
- Set up **GKE cluster** using Google Cloud Console or `gcloud` CLI.

### 2. Jenkins Configuration
- Installed plugins: Git, Docker, SonarQube Scanner, OWASP Dependency-Check, Trivy.
- Integrated SonarQube and OWASP with Jenkins via environment variables and webhooks.
- Created a pipeline (`Jenkinsfile`) to automate:
  - Code Checkout
  - Code Quality + Security Scans
  - Docker Image Build
  - Push to GCR
  - Deploy via ArgoCD

### 3. Security Scanning
- **SonarQube** → Code quality & bug detection  
- **OWASP Dependency Check** → Vulnerable dependencies  
- **Trivy** → Container image vulnerability scanning

### 4. Containerization
```bash
docker build -t gcr.io/<your-project-id>/netflix-app:v1 .
docker push gcr.io/<your-project-id>/netflix-app:v1
5. Deployment with ArgoCD
Deployed ArgoCD on GKE

Synced manifests from GitHub repo to GKE

Configured auto-sync for GitOps-style continuous deployment

6. Monitoring
Installed Prometheus and Grafana on GKE

Integrated Jenkins metrics & Kubernetes cluster stats

Created dashboards for pod health, CPU/memory usage, and build performance

📸 Screenshots
Add your project screenshots below 👇 (GCP Console, Jenkins dashboard, SonarQube results, Grafana dashboards, etc.)

Jenkins Pipeline	ArgoCD Sync	Grafana Dashboard

🧩 Key Learnings
Troubleshooting Jenkins–SonarQube connection taught me more than any tutorial 😅

YAML indent errors can break your entire deployment 🤦‍♂️

Proper webhook configuration is crucial for CI/CD sync

GCP + Kubernetes monitoring setup (Prometheus + Grafana) deepened my observability skills

🏁 Next Steps
Add automated Helm deployments

Integrate Slack notifications for pipeline stages

Enhance Prometheus alerts for build failures

📢 Author
👨‍💻 Shubham Dwivedi
Cloud & DevOps Enthusiast | Learning by Building | Exploring DevSecOps on GCP
📫 Connect on LinkedIn
