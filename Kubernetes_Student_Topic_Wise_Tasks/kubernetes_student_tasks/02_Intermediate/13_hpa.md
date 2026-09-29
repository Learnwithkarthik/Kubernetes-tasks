# Task 13 - Horizontal Pod Autoscaler

## Scenario
A web app should automatically scale when CPU usage increases.

## Requirements
1. Deploy `php-apache` using a CPU-consuming demo image suitable for HPA testing.
2. Set CPU requests on the container.
3. Create an HPA:
   - minimum replicas: 1
   - maximum replicas: 5
   - target CPU: 50%
4. Generate traffic from another pod.
5. Watch replicas increase.
6. Stop traffic and observe scale-down.

## Validation
```bash
kubectl get hpa -w
kubectl get deploy,pods -n student-lab
kubectl top pods -n student-lab
```

## Prerequisite
Metrics Server must be installed and working.

## Student question
Why will HPA often fail or show `<unknown>` when CPU requests are missing?
