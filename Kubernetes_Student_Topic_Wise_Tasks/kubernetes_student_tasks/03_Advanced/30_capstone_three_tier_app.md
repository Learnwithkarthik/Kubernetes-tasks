# Task 30 - Capstone: Secure Three-tier Application

## Scenario
Build a production-style mini application architecture using the Kubernetes concepts learned in class.

## Architecture
Client → Ingress → Frontend → Backend → Database

## Mandatory requirements
1. Separate namespace `capstone`.
2. Frontend Deployment: 2 replicas.
3. Backend Deployment: 2 replicas.
4. Database as StatefulSet: 1 replica.
5. ClusterIP Services for frontend, backend, and database.
6. Ingress exposes only frontend.
7. ConfigMap for non-sensitive configuration.
8. Secret for database credentials.
9. PVC for database data.
10. Requests and limits on every container.
11. ResourceQuota in namespace.
12. ServiceAccount for backend.
13. RBAC allowing backend SA to read only one ConfigMap.
14. NetworkPolicies:
    - only ingress/controller → frontend
    - frontend → backend only
    - backend → database only
15. Readiness and liveness probes.
16. HPA on frontend or backend.
17. Labels must be consistent and meaningful.
18. No privileged containers.

## Failure injection
Trainer should break any two items after deployment:
- Service selector
- Secret key
- backend port
- NetworkPolicy
- readiness probe

Students must troubleshoot and restore service.

## Final evidence
```bash
kubectl get all -n capstone
kubectl get ingress,networkpolicy,resourcequota -n capstone
kubectl get pvc -n capstone
kubectl auth can-i --list --as=system:serviceaccount:capstone:<backend-sa> -n capstone
```

## Submission
Students submit:
- all YAML manifests
- architecture diagram
- screenshots or terminal output
- short RCA for injected failures
