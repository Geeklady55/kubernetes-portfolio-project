\# Kubernetes Free Project – Cloud Engineering Portfolio



\*\*Author:\*\* Colleen Cummings  

Senior Technical Consultant | Cloud \& Integration Architect | AWS | Kubernetes | Linux | DevOps  



\---



\## Project Overview



This project demonstrates a working Kubernetes environment built using free tools:



• Docker Desktop  

• kind (Kubernetes in Docker)  

• kubectl  

• VS Code  

• GitHub  



The goal was to simulate a real support engineering environment including deployment, troubleshooting, observability, and scaling concepts.



\---



\## Architecture



Local Kubernetes cluster created using kind:



Docker → kind cluster → Kubernetes Deployment → Service → Web Application



\---



\## Features Demonstrated



\### Infrastructure

• Kubernetes cluster deployment  

• Containerized nginx application  

• Deployment configuration  

• Service exposure  



\### Observability

• Pod logs

• Events

• Metrics (kubectl top)

• Health checks



\### Reliability Engineering

• Liveness probes

• Readiness probes

• Resource limits

• Scaling replicas



\### Troubleshooting Skills

• Cluster connectivity issues

• YAML deployment problems

• Docker failures

• Context misconfiguration



\---



\## Key Commands Used



Cluster:



kind create cluster

kubectl get nodes



Deployment:



kubectl apply -f deployment.yaml

kubectl apply -f service.yaml



Monitoring:



kubectl get pods

kubectl describe pod <pod>

kubectl logs <pod>

kubectl top pods

kubectl get events





Troubleshooting:



kubectl cluster-info

kubectl config get-contexts

docker ps





\## Project Structure



kubernetes-free-project

│

├── app

│ ├── Dockerfile

│ └── index.html

│

├── k8s

│ ├── deployment.yaml

│ └── service.yaml

│

└── README.md



```text
           +-------------------+
           |   User Browser    |
           +-------------------+
                    |
                    v
           +-------------------+
           |   Kubernetes      |
           |     Service       |
           +-------------------+
                    |
                    v
           +-------------------+
           |   Deployment      |
           | nginx-deployment  |
           +-------------------+
              /            \
             v              v
      +-------------+   +-------------+
      |   Pod 1     |   |   Pod 2     |
      | nginx       |   | nginx       |
      +-------------+   +-------------+






\---



\## Skills Demonstrated



Cloud Engineering  

Kubernetes Administration  

Linux Troubleshooting  

Docker  

Infrastructure as Code concepts  

Production Support workflows  

Observability fundamentals  

Incident debugging  



\---



\## Lessons Learned



This project strengthened skills in:



• Kubernetes troubleshooting methodology  

• Container networking basics  

• Deployment debugging  

• Observability workflows  

• Infrastructure organization  



\---



\## Future Improvements



Add:



• Horizontal Pod Autoscaler

• Prometheus monitoring

• Grafana dashboards

• CI/CD pipeline

• Terraform infrastructure



\---



\## Author



Colleen Cummings  

Senior Cloud Engineer / Technical Consultant  



GitHub:

https://github.com/Geeklady55



\---



\## Purpose



This project was built as part of a cloud engineering portfolio to demonstrate hands-on Kubernetes operational knowledge.







