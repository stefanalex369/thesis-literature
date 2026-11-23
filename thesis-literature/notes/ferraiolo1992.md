# ferraiolo1992: Role-Based Access Controls

- **Reference:** Ferraiolo, D. F., & Kuhn, D. R. (1992). Role-Based Access Controls. In *Proceedings of the 15th National Computer Security Conference*, pp. 554–563.
- **Full text:** [`pdfs/ferraiolo1992.pdf`](../pdfs/ferraiolo1992.pdf) (published by NIST)
- **Topic:** Access control
- **Thesis chapter:** 5 (Access control, security and data protection)

## What it is

The paper that introduced role-based access control (RBAC). It argues that discretionary access control (DAC), where the owner of data decides who may access it, does not fit civilian and commercial organizations, where access should follow a person's job function. It gives a formal description based on three rules (role assignment, role authorization, transaction authorization) and discusses role hierarchies and separation of duties.

## What is relevant for my work

- **Why roles.** Permissions in my application follow job functions (training staff, trainer, client company representative), not the decision of whoever created a record. This is the paper's central argument.
- **What roles do not solve.** The paper does not address restricting access to particular records, such as a trainer seeing only their own cohorts. Doing that with roles alone would need one role per cohort and per client company ("role explosion"). I handle it with attributes, see hu2014.
- **Separation of duties.** Attendance and exam results are imported automatically. I apply the principle as privilege separation: only staff can correct an imported value, trainers and client users have read-only access, and every correction is written to an audit log.

## Limitations

The 1992 formalization is built around subjects executing transactions and only sketches hierarchies and constraints. For the RBAC0–RBAC3 models that map directly to database tables I use sandhu1996.
