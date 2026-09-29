# Task 17 - StorageClass

## Scenario
The platform team wants dynamic volume provisioning.

## Requirements
1. List all StorageClasses.
2. Identify the default StorageClass, if one exists.
3. Create a PVC that uses the default StorageClass.
4. Deploy a pod that mounts this claim.
5. Confirm a PV is dynamically created.
6. Explain `reclaimPolicy` and `volumeBindingMode`.

## Validation
```bash
kubectl get storageclass
kubectl get pv,pvc -A
```

## Challenge
If your kubeadm lab has no dynamic provisioner, document why the PVC stays Pending and what component is missing.
