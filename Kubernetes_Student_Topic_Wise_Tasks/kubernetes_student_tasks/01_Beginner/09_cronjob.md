# Task 09 - CronJob

## Scenario
The operations team needs a small task to run every minute.

## Requirements
1. Create CronJob `time-cron`.
2. Schedule it every minute.
3. Use `busybox:1.36`.
4. Print `Scheduled run` and current date.
5. Observe at least two Jobs created by the CronJob.
6. Suspend the CronJob.
7. Resume it.

## Validation
```bash
kubectl get cronjob,jobs,pods -n student-lab
kubectl describe cronjob time-cron -n student-lab
```
