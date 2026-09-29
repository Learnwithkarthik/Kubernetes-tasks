# Task 23 - NetworkPolicy

## Scenario
A three-tier application contains frontend, backend, and database pods. Traffic must be restricted.

## Requirements
1. Create namespace `netpol-demo`.
2. Deploy pods/services for:
   - frontend
   - backend
   - database
3. First prove all pods can communicate.
4. Apply default-deny ingress policy.
5. Allow only:
   - frontend → backend on port 8080
   - backend → database on port 5432
6. Ensure frontend cannot directly reach database.
7. Ensure unrelated pods cannot reach backend.
8. Document every test result.

## Validation
Use temporary curl/wget/netshoot pods and record:
- allowed path result
- denied path result

## Prerequisite
The CNI plugin must enforce NetworkPolicy (for example Calico/Cilium).
