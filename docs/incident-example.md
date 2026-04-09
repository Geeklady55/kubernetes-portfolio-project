\# Incident Example



\## Incident Title

Application unavailable due to Kubernetes API connectivity issue



\## Summary

During deployment validation, kubectl commands failed because the local Kubernetes API server was unreachable. This prevented manifest application and delayed testing.



\## Symptoms

\- `kubectl apply` failed

\- `kubectl cluster-info` failed

\- connection refused errors to local API endpoint

\- deployment validation could not complete



\## Impact

Application could not be deployed or validated in the local kind cluster.



\## Investigation Steps

1\. Checked kubectl error output

2\. Verified current kubectl context

3\. Checked whether the kind cluster still existed

4\. Verified Docker Desktop health

5\. Recreated the kind cluster

6\. Revalidated node readiness

7\. Reapplied manifests



\## Root Cause

The local Kubernetes API endpoint referenced by kubectl was no longer reachable because the underlying kind cluster had stopped or become unavailable.



\## Resolution

\- restarted Docker Desktop

\- recreated cluster

\- validated node readiness

\- redeployed manifests successfully



\## Commands Used



```powershell

docker ps

kind get clusters

kubectl config current-context

kubectl cluster-info

kind delete cluster

kind create cluster

kubectl get nodes

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml

