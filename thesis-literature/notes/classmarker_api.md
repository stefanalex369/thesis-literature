# classmarker_api: ClassMarker API and Webhooks

- **Reference:** ClassMarker. *ClassMarker API and Webhooks documentation*. Accessed 2026-11-23.
- **Full text:** web documentation:
  - API overview: https://www.classmarker.com/online-testing/api/
  - Webhooks: https://www.classmarker.com/online-testing/docs/webhooks/
- **Topic:** Platform documentation (online exams)
- **Thesis chapters:** 3 (API integration), 4 (Identity matching), 7 (Implementation)

## What it is

Documentation of how results of online exams taken in ClassMarker, the exam platform currently used in the case study, can be sent to or retrieved by other systems: webhooks that push each result as it is recorded, and an API secured with an API key and secret.

## What is relevant for my work

- **The fourth source system.** The thesis description speaks of "a separate platform for exams"; this is its documentation. Exam results are the outcome my reports relate course activity to.
- **Push, signed.** A webhook sends each result as JSON. ClassMarker signs the payload with HMAC-SHA256 using a secret known only to the account and my application, and sends the signature in the `X-Classmarker-Hmac-Sha256` header; I verify it before processing (owasp2025, A08). Failed deliveries are retried by ClassMarker, so processing must be idempotent (hohpe2003).
- **Identity.** Results have to be linked to the trainee. Which identifying fields a result carries (e-mail or other fields set up for the test) determines how reliable the match is, and I will document this in the data model chapter.
- **Integration style.** Webhooks for new results, the API for retrieving older results once, at start-up.

## Limitations

Commercial documentation. If the exam platform changes during the thesis, only this module of the application is affected, which is one argument for the canonical data model (hohpe2003).
