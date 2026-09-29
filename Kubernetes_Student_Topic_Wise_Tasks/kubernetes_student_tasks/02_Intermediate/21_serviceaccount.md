# Task 21 - ServiceAccount

## Scenario
A pod must use its own Kubernetes identity instead of the default ServiceAccount.

## Requirements
1. Create ServiceAccount `app-sa`.
2. Create a Role allowing only `get` and `list` on ConfigMaps.
3. Bind the Role to `app-sa`.
4. Create a pod using `serviceAccountName: app-sa`.
5. Verify which ServiceAccount is used.
6. Test permissions with `kubectl auth can-i`.

## Validation
```bash
kubectl get sa -n student-lab
kubectl get pod <pod-name> -n student-lab -o jsonpath='{.spec.serviceAccountName}'
kubectl auth can-i list configmaps -n student-lab --as=system:serviceaccount:student-lab:app-sa
```
