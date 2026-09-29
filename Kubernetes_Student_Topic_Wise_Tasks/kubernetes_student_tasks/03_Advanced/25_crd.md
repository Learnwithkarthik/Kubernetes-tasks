# Task 25 - CustomResourceDefinition

## Scenario
Your platform team wants to store a simple custom Kubernetes object called `Student`.

## Requirements
1. Create a CRD:
   - kind: `Student`
   - plural: `students`
   - group: `training.dsu.io`
   - version: `v1`
   - scope: Namespaced
2. Define fields:
   - `spec.name` string
   - `spec.course` string
   - `spec.level` string
3. Create at least two Student custom resources.
4. List them with kubectl.
5. Describe one custom resource.
6. Add printer columns if comfortable.

## Validation
```bash
kubectl get crd
kubectl api-resources | grep -i student
kubectl get students -A
```

## Student question
What is the difference between a CRD and a custom controller/operator?
