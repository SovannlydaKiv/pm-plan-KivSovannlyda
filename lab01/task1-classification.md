# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | It has a definite end date (week 14) and delivers a unique new platform. |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | Repeats every night with the same output and no end date; it is part of keeping the service running. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | It has a strict deadline (Dec 15) and achieves a one-time unique migration. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | This is continuous, repetitive daily work with no end date. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | Three related projects; the shared login and grade export are a benefit none delivers alone, so they are coordinated. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | This is an ongoing maintenance task repeated every month. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | It delivers a unique new capability within a specific future time frame. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | Continuous support and maintenance with no end date. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | It has a strict deadline (Jan 31) and produces a unique yearly document. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | A one-off endeavor limited to the summer break delivering a specific outcome. |

## Grey zones
- **Initiative 7 (Add multi-node scaling):** Is it just a maintenance release or a new project? It depends on whether the sponsor funds it as a separate endeavor with its own defined end date.
- **Initiative 9 (Annual IT report):** It is annual and repetitive, yet each report is unique with a strict deadline. Knowing if there is a specific budget or temporary team assigned would settle it.

## What our project hands over
At go-live in week 14, the Realtime Quiz project hands over the platform to the IT Operations team. IT Operations will be responsible for running the gicitc.com hosting, managing backups, and handling password resets. To do this successfully, they will need a deployment checklist, a runbook, and the production docker-compose files from the project team.