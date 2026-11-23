# sandhu1996: Role-Based Access Control Models

- **Reference:** Sandhu, R. S., Coyne, E. J., Feinstein, H. L., & Youman, C. E. (1996). Role-Based Access Control Models. *Computer*, 29(2), 38–47.
- **Full text:** publisher version paywalled (IEEE), not included. DOI: https://doi.org/10.1109/2.485845
- **Topic:** Access control (formal models)
- **Thesis chapter:** 5 (Access control, security and data protection)

## What it is

Defines the RBAC96 family: RBAC0 (users, roles, permissions, sessions), RBAC1 (adds role hierarchies), RBAC2 (adds constraints such as mutually exclusive roles) and RBAC3 (both).

## What is relevant for my work

- **Basis of my permission model.** RBAC0 maps directly to tables: `users`, `roles`, `permissions`, `user_roles`, `role_permissions`. I cite this paper for the model.
- **Hierarchy (RBAC1).** Staff inherit the read permissions of trainers. This is compatible with the privilege separation described in ferraiolo1992, because the permission to correct imported data belongs only to staff and is not inherited by anyone.
- **Which actions vs which records.** RBAC96 controls which actions a role may perform (for example "view attendance"). Which records the action applies to (only the trainer's own cohorts, only the client's own employees) is decided by attributes of the user and of the record, as in hu2014. I will enforce this filter in one place in the application's data access layer, so that no endpoint can skip it, and evaluate PostgreSQL row-level security as a second barrier.

## Limitations

Read through the university library; the publisher version is not open access.
