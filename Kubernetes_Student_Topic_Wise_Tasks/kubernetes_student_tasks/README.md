# Kubernetes Student Hands-on Task Pack

Designed as a topic-wise practice set from Beginner → Intermediate → Advanced.

## How to use
- Give students only the task files.
- Each file contains a scenario, requirements, validation steps, and optional hints.
- Students should create their own YAML manifests unless a task explicitly asks for an imperative command.
- Do not share solutions first. Ask students to prove their result using the validation commands.

## Suggested scoring
- Beginner: 10 marks/task
- Intermediate: 15 marks/task
- Advanced: 20 marks/task
- Bonus: 5 marks for clean YAML, labels, comments, and troubleshooting explanation.

## Important note
PodSecurityPolicy (PSP) was removed from Kubernetes starting with v1.25.
The pack therefore includes a modern Pod Security Admission (PSA) exercise and a short PSP-vs-PSA migration task.
