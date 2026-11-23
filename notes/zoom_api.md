# zoom_api: Zoom API, Webhooks and Server-to-Server OAuth

- **Reference:** Zoom Communications, Inc. *Zoom developer documentation*. Accessed 2026-11-23.
- **Full text:** web documentation:
  - API reference: https://developers.zoom.us/docs/api/
  - Webhooks: https://developers.zoom.us/docs/api/webhooks/
  - Server-to-Server OAuth: https://developers.zoom.us/docs/internal-apps/s2s-oauth/
  - E-mail display rules: https://developers.zoom.us/changelog/platform/zoom-api-email-address-display-rules/
- **Topic:** Platform documentation (videoconferencing)
- **Thesis chapters:** 3 (API integration), 7 (Implementation)

## What it is

The official documentation of Zoom's REST API, its webhooks (event notifications) and the Server-to-Server OAuth app type used for internal integrations.

## What is relevant for my work

- **Attendance data.** The participant report for a past meeting (`/report/meetings/{meetingId}/participants`) lists each join with its join time, leave time and duration. A trainee who reconnects appears several times, so the intervals have to be merged per person. For recurring meetings, each occurrence is identified by its own meeting UUID, while the meeting ID stays the same.
- **E-mail addresses are often missing.** Since March 2022, Zoom APIs and webhooks leave the e-mail empty for guest participants, meaning anyone not on the host's Zoom account. It is returned only in specific cases, the most useful being meeting registration. This is the main identity problem of my data model (see christen2012), and it leads to a concrete design choice: sessions are set up with registration, so that each participant's e-mail is known.
- **Webhooks.** Events such as the end of a meeting can trigger the attendance import instead of polling. Every webhook request carries a signature (HMAC-SHA256 over a timestamp and the request body, sent in the `x-zm-signature` header) that must be verified before the payload is processed (owasp2025, A08).
- **Authentication.** Server-to-Server OAuth with short-lived access tokens, see rfc6749.
- **Rate limits** decide how imports for many sessions are scheduled.

## Limitations

Commercial documentation that changes over time. I record the access dates and keep the Zoom integration in one isolated module.
