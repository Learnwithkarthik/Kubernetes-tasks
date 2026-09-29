# Task 27 - PSP Legacy to PSA Migration

## Scenario
You inherited an old document that uses PodSecurityPolicy. Your cluster is modern and does not support PSP.

## Requirements
1. Explain why PSP manifests do not work on Kubernetes v1.25+.
2. Identify the closest Pod Security Standards profiles:
   - privileged
   - baseline
   - restricted
3. Create a migration plan from an old restrictive PSP to namespace-level PSA.
4. Apply `warn` mode first.
5. Then move to `enforce`.
6. Document one workload change required to satisfy `restricted`.

## Deliverable
A short markdown note named `psp-migration-answer.md` containing:
- old approach
- new approach
- rollout plan
- rollback idea
