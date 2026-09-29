# Task 11 - StatefulSet

## Scenario
You need three stateful web pods with stable identities.

## Requirements
1. Create namespace `stateful-demo`.
2. Create a headless Service named `nginx`.
3. Create StatefulSet `web` with 3 replicas.
4. Pods must be named `web-0`, `web-1`, `web-2`.
5. Use `nginx:alpine`.
6. Verify stable DNS names for each pod.
7. Delete `web-1` and check whether its identity is preserved.

## Validation
```bash
kubectl get sts,pods,svc -n stateful-demo
kubectl exec -it -n stateful-demo <dns-test-pod> -- nslookup web-0.nginx
```

## Student question
Why is a headless Service useful for StatefulSets?
