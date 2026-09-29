# Task 29 - StatefulSet Storage Failure

## Scenario
A 3-replica StatefulSet is expected to create one PVC per pod, but one replica stays Pending.

## Requirements
1. Build a StatefulSet with `volumeClaimTemplates`.
2. Use 3 replicas.
3. Intentionally introduce a storage issue for one or all claims, such as an invalid/nonexistent StorageClass.
4. Diagnose why the pod is Pending.
5. Fix the storage configuration.
6. Confirm all three pods become Running.
7. Write unique data to each pod volume.
8. Restart the StatefulSet pods and prove the data remains.

## Validation
```bash
kubectl get sts,pods,pvc,pv -n stateful-demo
kubectl describe pod <pending-pod> -n stateful-demo
kubectl describe pvc <claim> -n stateful-demo
```
