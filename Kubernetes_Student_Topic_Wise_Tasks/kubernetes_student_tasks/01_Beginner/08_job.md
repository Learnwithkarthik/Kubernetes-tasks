# Task 08 - Job

## Scenario
A one-time batch task must run and complete successfully.

## Requirements
1. Create Job `hello-job`.
2. Use `busybox:1.36`.
3. Run a command that prints the current date, sleeps 5 seconds, then prints `Job Completed`.
4. Use `restartPolicy: Never`.
5. Wait for completion.
6. View the logs.

## Validation
```bash
kubectl get job,pods -n student-lab
kubectl logs -n student-lab job/hello-job
```

## Challenge
Create another Job with `completions: 3`.
