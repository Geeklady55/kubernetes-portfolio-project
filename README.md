\# Kubernetes Portfolio Project



\## Overview



This project demonstrates how to deploy a containerized application into a local Kubernetes cluster using free tools.



\## Technologies Used



\- Kubernetes

\- Docker

\- kubectl

\- kind

\- VS Code

\- GitHub



\## Project Structure



kubernetes-free-project



app → container application  

k8s → Kubernetes deployment files  

README.md → project documentation  



\## Features



\- Local Kubernetes cluster

\- Container deployment

\- NodePort service exposure

\- Health checks (future)

\- Scaling support



\## Deployment Steps



Create cluster:



kind create cluster



Build container:



docker build -t nginx-portfolio ./app



Load image:



kind load docker-image nginx-portfolio



Deploy:



kubectl apply -f k8s/



Check:



kubectl get pods

kubectl get svc



Access app:



kubectl port-forward service/nginx-service 8080:80



\## Author



Colleen Cummings  

Senior Technical Support Engineer  

Cloud \& Integration Architect



\## Purpose



This project demonstrates Kubernetes fundamentals including container deployment, service exposure, and cluster management.

