# Kubernetes Free Project

This project demonstrates how to build a free local Kubernetes environment using:

- kind
- kubectl
- Docker
- GitHub Actions

## Features
- Local Kubernetes cluster
- NGINX sample app
- Deployment and Service manifests
- GitHub workflow validation

## Run locally

### 1. Create cluster
kind create cluster --config k8s/kind-config.yaml

### 2. Build image
docker build -t my-nginx-app:1.0 ./app

### 3. Load image into kind
kind load docker-image my-nginx-app:1.0 --name free-cluster

### 4. Deploy
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

### 5. Access app
kubectl port-forward service/my-nginx-service 8080:80