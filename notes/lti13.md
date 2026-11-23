# lti13: Learning Tools Interoperability Core Specification 1.3

- **Reference:** 1EdTech Consortium (2019). *Learning Tools Interoperability Core Specification, Version 1.3*. Accessed 2026-11-23.
- **Full text:** free specification at https://www.imsglobal.org/spec/lti/v1p3/
- **Topic:** Education interoperability standards
- **Thesis chapters:** 2 (Background), 3 (Architecture)

## What it is

The current version of the main standard for connecting external tools to learning management systems. A user who is already in the LMS launches a tool; the LMS sends a signed message with the user's identity and course context, and services such as grade return can be used.

## What is relevant for my work

- **The standard alternative I have to discuss.** A reviewer will ask why I do not use the education standard for integration. LTI is built around the LMS as the center: the tool is launched from a course. In my case the data starts in the CRM (registrations, client companies) before any Moodle account exists, live sessions happen in Zoom and exams on a separate platform. LTI does not cover moving registration data into the LMS or collecting attendance from a videoconferencing platform, so it does not replace the integration my application performs.
- **Where it could still be used.** If the exam platform or a future tool supports LTI, launching it from Moodle would give one login and automatic grade return. I note this as an option, not as part of the implementation.

## Limitations

Read for its scope and model, not implemented.
