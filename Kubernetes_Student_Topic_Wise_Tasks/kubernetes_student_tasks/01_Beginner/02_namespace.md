# Task 02 - Namespace

## Scenario
A company wants separate namespaces for development and testing.

## Requirements
1. Create namespaces `dev-team` and `test-team`.
2. Deploy one NGINX pod in each namespace.
3. Use the same pod name `frontend` in both namespaces.
4. Prove that both pods can exist with the same name.
5. List resources only from `dev-team`.
6. Set your current kubectl context namespace to `dev-team`.

## Validation
```bash
kubectl get pods -n dev-team
kubectl get pods -n test-team
kubectl config view --minify
```
