# Task 18 - Ingress

## Scenario
Two web applications must be exposed using different URL paths.

## Requirements
1. Deploy two applications:
   - `app1`
   - `app2`
2. Create Services for both.
3. Configure Ingress:
   - `/app1` → app1 service
   - `/app2` → app2 service
4. Test both routes.
5. Inspect the Ingress rules.

## Validation
```bash
kubectl get ingress -n student-lab
kubectl describe ingress -n student-lab
```

## Prerequisite
An Ingress Controller must already be installed.

## Student question
What is the difference between an Ingress resource and an Ingress Controller?
