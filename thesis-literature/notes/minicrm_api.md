# minicrm_api: MiniCRM API

- **Reference:** MiniCRM. *MiniCRM API*. Accessed 2026-11-23.
- **Full text:** web documentation at https://www.minicrm.io/help/api/ (links to the full API and integration manual)
- **Topic:** Platform documentation (CRM)
- **Thesis chapters:** 3 (API integration), 7 (Implementation)

## What it is

The official entry page for MiniCRM's integration options: a REST API and XML synchronization. Authentication, resources and limits are described in the linked manual.

## What is relevant for my work

- **System of record for registrations.** Registrations, trainees and client companies are created and edited in the CRM. My application reads them and never writes back. One system of record per type of data avoids conflicting edits; this is a design decision I will state and justify.
- **How changes are detected.** Whether new and changed registrations can be pushed to my application or have to be found by periodic polling (with the time of the last successful import) depends on what the API offers. I will document the endpoints and the method used, with the version of the manual, in the implementation chapter.

## Limitations

The public page is brief. Technical details will be cited from the API manual, with its version and date.
