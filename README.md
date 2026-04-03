\# Kubernetes Portfolio Project



\## Overview

This project demonstrates deploying a containerized application into Kubernetes using Docker, kind, and kubectl.



\## Technologies

Kubernetes

Docker

kubectl

kind

VS Code

GitHub



\## Run steps



kind create cluster



docker build -t nginx-portfolio ./app



kind load docker-image nginx-portfolio



kubectl apply -f k8s/



kubectl get pods

kubectl get svc

