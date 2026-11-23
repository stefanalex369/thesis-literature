# owaspapi2023: OWASP API Security Top 10 – 2023

- **Reference:** OWASP Foundation (2023). *OWASP API Security Top 10 – 2023*. Accessed 2026-11-23.
- **Full text:** free web document at https://owasp.org/API-Security/editions/2023/en/0x11-t10/
- **Topic:** API security
- **Thesis chapters:** 5 (Security), 7 (Evaluation)

## What it is

The OWASP list of the ten most critical security risks specific to APIs, as opposed to web applications in general (owasp2025).

## What is relevant for my work

- **API1:2023 Broken Object Level Authorization (BOLA).** An endpoint receives an object ID (`/trainees/{id}`) and returns the object without checking that this user may see this particular object. It is the precise name for the main risk of my application's internal API, and the reason the scope check (hu2014) sits in the data access layer rather than in each endpoint.
- **API10:2023 Unsafe Consumption of APIs.** My application also consumes three or four external APIs. Data received from them is validated before it is stored, and HTTP calls to them have timeouts, as for any untrusted input.
- **API4:2023 Unrestricted Resource Consumption** applies in the other direction: report exports over large date ranges need limits.

## Limitations

Awareness list like owasp2025; the concrete tests are defined in the evaluation chapter.
