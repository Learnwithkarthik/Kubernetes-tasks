# Task 04 - ReplicaSet

## Scenario
Your trainer wants you to understand ReplicaSet directly before relying on Deployments.

## Requirements
1. Create a ReplicaSet named `web-rs`.
2. Use image `nginx:alpine`.
3. Maintain 3 replicas.
4. Use selector `app=web-rs`.
5. Delete one managed pod.
6. Create one extra standalone pod with the same matching label and observe the ReplicaSet behavior.

## Validation
```bash
kubectl get rs,pods -n student-lab --show-labels
kubectl describe rs web-rs -n student-lab
```

## Student question
What happens if more pods match the ReplicaSet selector than the desired replica count?
