🚀 Blue-Green CI/CD Deployment using Jenkins, Docker & Kubernete


📌 Project Overview

This project demonstrates a Production-Ready Blue-Green Deployment Strategy implemented using:

🔹 Jenkins – CI/CD automation

🔹 Docker – Containerization

🔹 Kubernetes – Container orchestration

🔹 GitHub – Source code management

The objective is to achieve Zero Downtime Deployment while releasing new application versions.


🔄 How Blue-Green Deployment Works
🔵 Blue Environment

Currently serving production traffic

Stable version

🟢 Green Environment

New version deployed

Tested before going live

Traffic Switching

Kubernetes Service selector updates:

selector:
  version: green


Traffic shifts instantly from Blue → Green without downtime.

⚙️ CI/CD Pipeline Flow
Developer Push
      ↓
Jenkins Build
      ↓
Docker Image Build
      ↓
Push to Docker Hub
      ↓
Deploy Green in Kubernetes
      ↓
Switch Service Traffic

📂 Project Structure
blue-green-ci-cd/
│
├── app/
│   └── index.html
│
├── Dockerfile
├── Jenkinsfile
│
├── k8s/
│   ├── blue-deployment.yaml
│   ├── green-deployment.yaml
│   └── service.yaml
│
└── README.md

🌐 Application Output
🔵 Version 1 – Blue Environment
Version 1 - Blue Environment

🟢 Version 2 – Green Environment
Version 2 - Green Environment


Users experience zero downtime during switching.

🛠 Technologies Used
Tool	Purpose
Jenkins	CI/CD Automation
Docker	Containerization
Kubernetes	Deployment & Traffic Switching
GitHub	Source Code Management
🔁 Rollback Strategy

If the Green deployment fails:

kubectl patch service my-service -p '{"spec":{"selector":{"version":"blue"}}}'


Traffic immediately switches back to Blue.

🎯 Key Features

✔ Zero Downtime Deployment
✔ Instant Rollback
✔ Automated CI/CD Pipeline
✔ Production-Ready Strategy
✔ Scalable Infrastructure

📊 Real-World Relevance

This deployment strategy is commonly used by large tech companies to ensure seamless updates in production environments.

🧠 Skills Demonstrated

CI/CD Pipeline Automation

Docker Image Lifecycle Management

Kubernetes Deployments & Services

Blue-Green Deployment Strategy

DevOps Best Practices


👨‍💻 Author

Chethan B.S
DevOps Enthusiast 🚀
