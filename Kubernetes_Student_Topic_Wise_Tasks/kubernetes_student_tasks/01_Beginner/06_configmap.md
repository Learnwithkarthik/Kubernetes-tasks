# Task 06 - ConfigMap

## Scenario
Application configuration should not be hardcoded in the container image.

## Requirements
1. Create ConfigMap `app-config`.
2. Store:
   - `APP_ENV=dev`
   - `APP_COLOR=blue`
3. Create a pod that reads both values as environment variables.
4. Verify the values inside the pod.
5. Create another ConfigMap from a file called `app.properties`.
6. Mount that ConfigMap as files under `/etc/appconfig`.

## Validation
```bash
kubectl get cm -n student-lab
kubectl exec -n student-lab <pod-name> -- printenv
kubectl exec -n student-lab <pod-name> -- ls -l /etc/appconfig
```
