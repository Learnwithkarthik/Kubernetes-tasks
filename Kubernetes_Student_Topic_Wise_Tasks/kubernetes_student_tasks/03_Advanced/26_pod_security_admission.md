# Task 26 - Pod Security Admission

## Scenario
The security team wants to prevent privileged workloads in a namespace.

## Requirements
1. Create namespace `secure-demo`.
2. Apply Pod Security Admission labels to enforce the `restricted` profile.
3. Try to create a pod that:
   - runs privileged
   - runs as root
   - allows privilege escalation
4. Observe which settings are rejected.
5. Modify the manifest to comply with the restricted profile.
6. Successfully deploy the corrected pod.

## Validation
```bash
kubectl get ns secure-demo --show-labels
kubectl get events -n secure-demo --sort-by=.lastTimestamp
```

## Note
PodSecurityPolicy (PSP) was removed in Kubernetes v1.25. PSA is the built-in replacement mechanism for namespace-level pod security standards.
