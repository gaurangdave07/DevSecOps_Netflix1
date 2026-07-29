# 🎬 DevSecOps Netflix Clone CI/CD Pipeline

A complete **DevSecOps End-to-End CI/CD Pipeline** for deploying a Netflix Clone application using **Jenkins, SonarQube, OWASP Dependency Check, Trivy, Docker, Kubernetes, Prometheus, and Grafana** on **AWS EC2**.

This project demonstrates modern DevSecOps practices by integrating security scanning, automated testing, containerization, monitoring, and continuous deployment.

---

## 📌 Project Architecture

```text
                    GitHub
                       │
                       ▼
                 Jenkins Pipeline
                       │
     ┌─────────────────┼──────────────────┐
     │                 │                  │
     ▼                 ▼                  ▼
 SonarQube      OWASP Dependency      Trivy Scan
  (SAST)            Check (SCA)      (Container Scan)
     │                 │                  │
     └─────────────────┼──────────────────┘
                       ▼
                 Docker Build
                       ▼
              Push to Docker Hub
                       ▼
             Kubernetes Deployment
                       ▼
              Netflix Clone Running
                       │
         ┌─────────────┴─────────────┐
         ▼                           ▼
    Prometheus                 Grafana
                       │
                 Email Notification
```

---

# 🚀 Features

- ✅ End-to-End DevSecOps Pipeline
- ✅ Jenkins CI/CD Automation
- ✅ GitHub Integration
- ✅ SonarQube Static Code Analysis (SAST)
- ✅ OWASP Dependency Check (SCA)
- ✅ Trivy Filesystem & Docker Image Scanning
- ✅ Docker Containerization
- ✅ Docker Hub Image Repository
- ✅ Kubernetes Deployment
- ✅ Prometheus Monitoring
- ✅ Grafana Dashboards
- ✅ Jenkins Email Notifications
- ✅ AWS EC2 Deployment

---

# 🛠️ Tech Stack

| Category | Technology |
|-----------|------------|
| Frontend | React.js |
| Build Tool | Vite |
| CI/CD | Jenkins |
| Source Code | GitHub |
| Static Analysis | SonarQube |
| Dependency Scan | OWASP Dependency Check |
| Vulnerability Scan | Trivy |
| Containerization | Docker |
| Container Registry | Docker Hub |
| Orchestration | Kubernetes |
| Monitoring | Prometheus |
| Visualization | Grafana |
| Cloud | AWS EC2 |
| OS | Ubuntu 22.04 |

---

# 📂 Project Structure

```
Netflix/
│
├── src/
├── public/
├── Dockerfile
├── package.json
├── nginx.conf
├── Jenkinsfile
├── Kubernetes/
│   ├── deployment.yaml
│   └── service.yaml
└── README.md
```

---

# ⚙️ CI/CD Pipeline

The Jenkins pipeline performs the following stages:

1. Checkout Source Code
2. Install Dependencies
3. SonarQube Analysis
4. Quality Gate Validation
5. OWASP Dependency Check
6. Trivy Filesystem Scan
7. Docker Image Build
8. Docker Image Scan
9. Push Image to Docker Hub
10. Deploy Docker Container
11. Deploy to Kubernetes
12. Send Email Notification

---

# 🔒 Security Scanning

### SonarQube

- Static Application Security Testing (SAST)
- Code Smells
- Bugs
- Vulnerabilities
- Code Coverage

---

### OWASP Dependency Check

- Detect vulnerable libraries
- Generate Dependency Report
- CVE Analysis

---

### Trivy

Filesystem Scan

```bash
trivy fs .
```

Docker Image Scan

```bash
trivy image <docker-image>
```

---

# 🐳 Docker

## Build Image

```bash
docker build -t netflix .
```

## Run Container

```bash
docker run -d -p 8081:80 netflix
```

Application URL

```
http://<Public-IP>:8081
```

---

# ☸️ Kubernetes Deployment

Deploy Application

```bash
kubectl apply -f Kubernetes/deployment.yaml
kubectl apply -f Kubernetes/service.yaml
```

Verify

```bash
kubectl get all
```

---

# 📊 Monitoring

## Prometheus

Collects metrics from

- Jenkins
- Node Exporter
- Kubernetes Nodes

Default Port

```
9090
```

---

## Grafana

Visualizes

- CPU Usage
- Memory Usage
- Disk Usage
- Jenkins Metrics
- Kubernetes Metrics

Default Port

```
3000
```

Recommended Dashboards

- 1860 (Node Exporter)
- 9964 (Jenkins)

---

# 📧 Email Notification

Jenkins automatically sends an email after every pipeline execution containing

- Build Status
- Build Number
- Console Log
- Trivy Reports
- Dependency Reports

---

# ☁️ AWS Infrastructure

| Server | Purpose |
|---------|----------|
| Jenkins Server | CI/CD |
| Monitoring Server | Prometheus + Grafana |
| Kubernetes Master | Control Plane |
| Kubernetes Worker | Application Deployment |

---

# 📸 Screenshots

Add screenshots here

- EC2 Instance<img width="1121" height="776" alt="aws_ec2" src="https://github.com/user-attachments/assets/d5e2bc10-70fd-415f-95dc-1b456d5ab40b" />

- SonarQube Report
- OWASP Report
- Trivy Report
- Docker Hub Repository
- Kubernetes Pods
- Prometheus Dashboard
- Grafana Dashboard
- Running Netflix Application

---

# 🚀 Getting Started

Clone Repository

```bash
git clone https://github.com/gaurangdave07/Netflix.git
```

Move into project

```bash
cd Netflix
```

Install dependencies

```bash
npm install
```

Run locally

```bash
npm run dev
```

Build Production

```bash
npm run build
```

---

# 📈 Future Improvements

- GitHub Actions Pipeline
- Helm Charts
- ArgoCD GitOps
- Terraform Infrastructure
- AWS EKS Deployment
- HashiCorp Vault Integration
- Slack Notifications
- Kubernetes Ingress
- SSL with Let's Encrypt

---

# 👨‍💻 Author

**Gaurang Dave**

📧 Email: Your Email

💼 LinkedIn: https://linkedin.com/in/your-profile

🐙 GitHub: https://github.com/gaurangdave07

---

# ⭐ Support

If you found this project helpful, please give it a ⭐ on GitHub!

---

# 📜 License

This project is for educational and learning purposes.
