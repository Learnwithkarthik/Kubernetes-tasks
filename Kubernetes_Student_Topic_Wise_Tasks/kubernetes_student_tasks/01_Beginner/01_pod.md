# Task 01 - Pod

## Scenario
Your team needs a simple NGINX pod for a quick connectivity test.

## Requirements
1. Create namespace `student-lab`.
2. Create a Pod named `web-pod` using image `nginx:alpine`.
3. Add label `app=web`.
4. Expose container port `80`.
5. Add environment variable `ENV=training`.
6. Verify the pod is Running.
7. Print the environment variable from inside the pod.
8. Display the pod IP and node name.

## Validation
```bash
kubectl get pod web-pod -n student-lab -o wide
kubectl get pod web-pod -n student-lab --show-labels
kubectl exec -n student-lab web-pod -- printenv ENV
```

## Challenge
Delete the pod and recreate it using a YAML manifest instead of an imperative command.
