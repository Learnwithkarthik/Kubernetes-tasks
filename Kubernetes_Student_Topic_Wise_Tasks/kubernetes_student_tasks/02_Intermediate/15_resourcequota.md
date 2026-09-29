# Task 15 - ResourceQuota

## Scenario
The development namespace must not consume unlimited cluster resources.

## Requirements
1. Create namespace `quota-demo`.
2. Create ResourceQuota with:
   - requests.cpu: 2
   - requests.memory: 2Gi
   - limits.cpu: 4
   - limits.memory: 4Gi
   - persistentvolumeclaims: 5
   - requests.storage: 20Gi
3. Try creating a pod without resource requests/limits.
4. Record the error.
5. Fix the pod and create it successfully.
6. Display quota usage.

## Validation
```bash
kubectl describe quota -n quota-demo
kubectl get resourcequota -n quota-demo
```
