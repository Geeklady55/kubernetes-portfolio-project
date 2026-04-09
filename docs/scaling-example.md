\# Scaling Example



\## Objective

Demonstrate that the application can scale from a single replica to multiple replicas to improve resilience and availability.



\## Deployment Change



Replica count increased from:



```yaml

replicas: 1



yaml

replicas: 2



Command Used



kubectl apply -f deployment.yaml

kubectl get pods



Results





Kubernetes created multiple pod replicas for the same deployment.



Operational Value



Scaling improves:



availability

resilience

maintenance flexibility

load handling capability

Future Enhancement



Horizontal Pod Autoscaler can be added to scale based on CPU or memory utilization.



Validation Commands

kubectl get deployment nginx-deployment

kubectl get pods -o wide

kubectl describe deployment nginx-deployment

