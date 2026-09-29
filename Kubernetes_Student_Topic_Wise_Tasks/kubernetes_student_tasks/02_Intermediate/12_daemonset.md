# Task 12 - DaemonSet

## Scenario
A log collection agent must run on every worker node.

## Requirements
1. Create DaemonSet `node-agent`.
2. Use image `busybox:1.36`.
3. Run a long-lived command such as `sleep 3600`.
4. Add label `app=node-agent`.
5. Verify one pod is scheduled per eligible node.
6. Add a new worker label and inspect whether pod placement changes.

## Validation
```bash
kubectl get ds,pods -n student-lab -o wide
kubectl describe ds node-agent -n student-lab
```

## Challenge
Make it run only on nodes labeled `agent=true`.
