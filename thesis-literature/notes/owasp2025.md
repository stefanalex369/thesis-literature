# owasp2025: OWASP Top 10:2025

- **Reference:** OWASP Foundation (2025). *OWASP Top 10:2025*. Accessed 2026-11-23.
- **Full text:** free web document at https://owasp.org/Top10/2025/
- **Topic:** Web application security
- **Thesis chapters:** 5 (Security), 7 (Evaluation)

## What it is

The current OWASP list of the ten most critical web application security risks, built from vulnerability data and a community survey.

## What is relevant for my work

- **A01:2025 Broken Access Control is ranked first**, and it is the main risk in my application: a trainer or client user reaching records outside their scope, for example by changing an ID in a URL. The API-specific form of this risk is API1:2023 in owaspapi2023.
- **A02:2025 Security Misconfiguration and A04:2025 Cryptographic Failures:** self-hosted deployment (HTTPS only, secure headers, no default credentials) and storage of API secrets.
- **A05:2025 Injection:** parameterized queries for all PostgreSQL access, and an allowlist for report filter and sort parameters.
- **A07:2025 Authentication Failures:** login for staff, trainers and client users.
- **A08:2025 Software or Data Integrity Failures:** incoming webhooks from Zoom and from the exam platform are signed (HMAC-SHA256); payloads whose signature or timestamp does not verify are rejected.
- **A09:2025 Security Logging & Alerting Failures:** an audit log of who viewed or changed trainee data, which also supports GDPR accountability.

## Use in the evaluation

The list is an awareness document, not a test standard, so I do not use it as a checklist. Instead, the evaluation chapter will contain concrete tests for the categories above: an automated matrix that calls every endpoint as each role and checks that a trainer of one cohort cannot read another cohort and a client user cannot read another company's trainees (A01); webhook requests with a modified body, a wrong signature and an old timestamp, all of which must be rejected (A08); and report parameters with injected values (A05).

## Limitations

The categories are broad; the test cases are my own selection for this application.
