# Task 16 - PersistentVolume and PersistentVolumeClaim

## Scenario
An application needs persistent storage that survives pod deletion.

## Requirements
1. Create a PersistentVolume `student-pv` with 1Gi capacity.
2. Use a hostPath only if this is a training/lab cluster.
3. Create PVC `student-pvc` requesting 500Mi.
4. Mount it into a pod at `/data`.
5. Write `hello persistent world` into `/data/message.txt`.
6. Delete the pod.
7. Create a second pod using the same PVC.
8. Prove the file still exists.

## Validation
```bash
kubectl get pv,pvc
kubectl exec -n student-lab <pod-name> -- cat /data/message.txt
```
