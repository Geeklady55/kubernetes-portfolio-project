\# Failure Simulation



\## Objective

Demonstrate Kubernetes self-healing by intentionally deleting a running pod and observing automatic recovery.



\## Test Procedure



\### Step 1: Identify running pods



```powershell

kubectl get pods





Step 2: Delete one pod



kubectl delete pod <pod-name>



Step 3: Watch recovery



kubectl get pods -w

Expected Result



Kubernetes detects the missing pod and automatically creates a replacement pod to maintain the desired replica count.





Why This Matters



This validates:



self-healing behavior

deployment reconciliation

workload resilience

Operational Value



This is a core production reliability behavior and demonstrates that the platform can recover from individual pod loss without manual intervention.



Example Support Narrative



A production pod was terminated unexpectedly. Because the workload was managed by a deployment with multiple replicas, Kubernetes automatically scheduled a replacement pod and restored the desired state.



Validation Commands

kubectl get pods

kubectl describe deployment nginx-deployment

kubectl get events

