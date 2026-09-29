# Task 19 - Endpoints and EndpointSlice

## Scenario
A Service exists, but users cannot reach the application.

## Requirements
1. Create Deployment with label `app=backend`.
2. Intentionally create a Service with selector `app=back-end`.
3. Check Service Endpoints/EndpointSlices.
4. Explain why no backend endpoints appear.
5. Fix the selector.
6. Verify endpoints are populated.
7. Delete one backend pod and watch endpoint changes.

## Validation
```bash
kubectl get svc,endpoints,endpointslices -n student-lab
kubectl describe svc <service-name> -n student-lab
```

## Troubleshooting goal
Students must identify the label-selector mismatch without being told exactly where the issue is.
