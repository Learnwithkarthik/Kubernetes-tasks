# Task 05 - Service

## Scenario
The frontend pods need a stable network endpoint.

## Requirements
1. Use an existing Deployment with label `app=frontend`.
2. Create ClusterIP Service `frontend-svc`.
3. Service port must be `80`.
4. Target port must be `80`.
5. Start a temporary BusyBox pod and test DNS resolution.
6. Access the Service using:
   - short name
   - namespace-qualified name
   - full cluster DNS name

## Validation
```bash
kubectl get svc,endpoints -n student-lab
kubectl run dns-test --rm -it --image=busybox:1.36 -n student-lab -- sh
```

## DNS names to test
- `frontend-svc`
- `frontend-svc.student-lab`
- `frontend-svc.student-lab.svc.cluster.local`
