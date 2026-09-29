# Task 22 - User and Group RBAC

## Scenario
All members of group `developers` should be able to read pods in `dev-team`.

## Requirements
1. Create Role `developer-reader`.
2. Bind it to group `developers`.
3. Test with an impersonated user who belongs to that group.
4. Prove the user can list pods.
5. Prove the user cannot delete pods.
6. Explain where Kubernetes user/group identity normally comes from.

## Validation
```bash
kubectl auth can-i list pods -n dev-team --as=alice --as-group=developers
kubectl auth can-i delete pods -n dev-team --as=alice --as-group=developers
```
