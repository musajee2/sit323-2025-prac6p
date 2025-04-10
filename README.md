# SIT323 Kubernetes Deployment

## Overview
This repo contains the deployment files for a Node.js application deployed on Kubernetes.

## Steps to Deploy

### Step 1: Enable Kubernetes
- Install Docker Desktop.
- Enable Kubernetes in Docker Desktop settings.

### Step 2: Build Docker Image
```bash
docker build -t node-k8s-app:latest .
docker tag node-k8s-app:latest yourdockerhubusername/node-k8s-app:latest
docker push yourdockerhubusername/node-k8s-app:latest
```
### Step 3: Kubernetes Deployment & Service
Deploy your app using:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### Step 4: Verify and Access Application
```bash
kubectl get deployments
kubectl get services
```
open http://localhost:31000 to see your app.
