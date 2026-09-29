# Task 07 - Secret

## Scenario
A database username and password must be passed to a pod securely.

## Requirements
1. Create Secret `db-secret`.
2. Store:
   - username: `student`
   - password: `training123`
3. Inject them as environment variables into a pod.
4. Verify them from inside the pod.
5. Inspect the Secret using YAML and identify how Kubernetes stores the values.
6. Decode one value manually.

## Validation
```bash
kubectl get secret db-secret -n student-lab -o yaml
kubectl exec -n student-lab <pod-name> -- printenv DB_USER
```

## Student question
Is base64 encryption? Explain.
