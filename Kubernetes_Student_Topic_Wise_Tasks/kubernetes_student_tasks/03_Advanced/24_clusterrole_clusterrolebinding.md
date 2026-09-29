# Task 24 - ClusterRole and ClusterRoleBinding

## Scenario
An operations user must be able to view nodes and pods across all namespaces without modification rights.

## Requirements
1. Create ClusterRole `ops-viewer`.
2. Allow:
   - get/list/watch nodes
   - get/list/watch pods
3. Bind it to user `opsuser`.
4. Confirm access across namespaces.
5. Confirm `opsuser` cannot delete nodes or pods.
6. Compare this with using the built-in `view` ClusterRole.

## Validation
```bash
kubectl auth can-i list nodes --as=opsuser
kubectl auth can-i list pods -A --as=opsuser
kubectl auth can-i delete pods -n kube-system --as=opsuser
```
