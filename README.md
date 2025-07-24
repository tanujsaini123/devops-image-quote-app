# 📸 Inspirational Image Quote Web App with CI/CD & Kubernetes

This is a DevOps project that serves random inspirational quotes and images using a Flask backend. The app is containerized with Docker, deployed using Kubernetes, and integrated with Jenkins for CI/CD automation.

---

## 🌟 Features

- Random quote and image display on every refresh.
- Built using **Python Flask**.
- Containerized using **Docker**.
- Deployed to **Kubernetes** using `deployment.yaml` and `service.yaml`.
- CI/CD pipeline with **Jenkins**.
- Images and quotes auto-refreshed on page reload.

---

## 🗂️ Project Structure

```
devops-image-quote-app/
│
├── backend/
│   ├── app.py                 # Flask backend
│   └── static/images/         # Inspirational images
│       ├── image1.png
│       ├── image2.png
│       └── image3.png
│
├── Dockerfile                 # Builds the image
├── Jenkinsfile                # CI/CD pipeline steps
├── docker-compose.yml         # Optional for local Docker testing
│
├── k8s/
│   ├── deployment.yaml        # Kubernetes Deployment
│   └── service.yaml           # Kubernetes Service
│
└── kindcluster/
    └── config.yml             # KIND cluster config (optional)
```

---

## 🐳 Docker Instructions

### ✅ Build Docker Image

```bash
docker build -t image-quote-app:latest .
```

### ✅ Run Locally with Docker

```bash
docker run -p 5000:5000 image-quote-app
```

Then open: [http://localhost:5000](http://localhost:5000)

---

## ☸️ Kubernetes Deployment

### ✅ Apply K8s Manifests

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

### ✅ Check Resources

```bash
kubectl get pods
kubectl get svc
```

### ✅ Port Forward to Access the App

```bash
kubectl port-forward svc/image-quote-service 5000:5000
```

Then open: [http://localhost:5000](http://localhost:5000)

---

## 🔧 Jenkins CI/CD Pipeline

### Jenkinsfile Pipeline Stages:
- Clone code from GitHub
- Build Docker image
- Push to DockerHub (optional)
- Deploy to Kubernetes cluster

Make sure Jenkins has:
- Docker access
- `kubectl` configured
- Proper GitHub and Docker credentials

---

## 📸 Sample Output

Every time you open the browser or click "🔁 Refresh", you get:

- ✨ A motivational quote
- 🖼️ A random image
  
---

## 🔗 Author

**Tanuj Saini**  
GitHub: [@tanujsaini123](https://github.com/tanujsaini123)  
Project Repo: [devops-image-quote-app](https://github.com/tanujsaini123/devops-image-quote-app)

---

## 🚀 “Dream it. Wish it. Do it.” — Unknown
