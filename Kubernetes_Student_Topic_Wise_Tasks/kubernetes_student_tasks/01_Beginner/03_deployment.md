# Task 03 - Deployment

## Scenario
You need a highly available web application.

## Requirements
1. Create Deployment `frontend-deploy` in `student-lab`.
2. Use image `nginx:1.27-alpine`.
3. Run 3 replicas.
4. Add label `app=frontend`.
5. Confirm the Deployment created a ReplicaSet.
6. Delete one pod manually and observe what happens.
7. Scale the Deployment from 3 to 5 replicas.

## Validation
```bash
kubectl get deploy,rs,pods -n student-lab
kubectl get pods -n student-lab -l app=frontend
```

## Student question
Why did the deleted pod come back automatically?
