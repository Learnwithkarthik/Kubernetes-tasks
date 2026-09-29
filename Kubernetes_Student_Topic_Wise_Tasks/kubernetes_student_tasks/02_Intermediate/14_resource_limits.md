# Task 14 - Requests and Limits

## Scenario
A namespace has limited compute capacity, so application containers must declare resources.

## Requirements
1. Create Pod `resource-demo`.
2. Configure:
   - requests.cpu: `100m`
   - requests.memory: `64Mi`
   - limits.cpu: `200m`
   - limits.memory: `128Mi`
3. Verify the settings.
4. Change the memory limit to a very low value for a memory-consuming container and observe behavior.
5. Explain `OOMKilled`.

## Validation
```bash
kubectl describe pod resource-demo -n student-lab
kubectl get pod resource-demo -n student-lab -o yaml
```
