# Task 10 - Node Basics

## Scenario
You are checking where workloads are running.

## Requirements
1. List all nodes with extra details.
2. Display labels on every node.
3. Identify one worker node.
4. Add label `workload=training` to that node.
5. Create a pod using `nodeSelector` so it lands on that node.
6. Confirm the assigned node.
7. Remove the label after the test.

## Validation
```bash
kubectl get nodes -o wide
kubectl get nodes --show-labels
kubectl get pod -n student-lab -o wide
```
