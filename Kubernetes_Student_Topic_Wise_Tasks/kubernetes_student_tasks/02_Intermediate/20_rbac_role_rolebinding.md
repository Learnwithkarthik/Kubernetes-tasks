# Task 20 - Role and RoleBinding

## Scenario
Developer `student1` should be allowed to view pods in `dev-team` but must not delete them.

## Requirements
1. Create Role `pod-reader` in `dev-team`.
2. Allow `get`, `list`, `watch` on pods.
3. Bind the Role to user `student1`.
4. Test permissions using `kubectl auth can-i`.
5. Confirm:
   - list pods = yes
   - delete pods = no
   - access pods in `test-team` = no

## Validation
```bash
kubectl auth can-i list pods -n dev-team --as=student1
kubectl auth can-i delete pods -n dev-team --as=student1
kubectl auth can-i list pods -n test-team --as=student1
```
