# Task 28 - Multi-object Troubleshooting

## Scenario
A Deployment is Running, but the application is unavailable.

## Broken design
The trainer should intentionally introduce at least three of these problems:
- Service selector mismatch
- wrong targetPort
- readiness probe failure
- missing ConfigMap
- bad Secret key reference
- Ingress path mismatch
- NetworkPolicy blocking traffic

## Student objective
Troubleshoot without recreating everything from scratch.

## Required investigation commands
```bash
kubectl get all -n student-lab
kubectl describe pod <pod> -n student-lab
kubectl logs <pod> -n student-lab
kubectl get svc,endpoints,endpointslices -n student-lab
kubectl get events -n student-lab --sort-by=.lastTimestamp
kubectl get networkpolicy -n student-lab
```

## Deliverable
Students must submit:
1. root cause(s)
2. commands used
3. fix applied
4. evidence after fix
