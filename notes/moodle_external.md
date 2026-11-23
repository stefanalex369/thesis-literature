# moodle_external: Moodle External Services (Web Services) API

- **Reference:** Moodle Pty Ltd. *External Services API*. Moodle Developer Resources. Accessed 2026-11-23.
- **Full text:** web documentation at https://moodledev.io/docs/apis/subsystems/external
- **Topic:** Platform documentation (LMS)
- **Thesis chapters:** 3 (API integration), 7 (Implementation)

## What it is

The official documentation of how Moodle exposes functions to external systems. Functions are grouped into services, and a client calls them over a protocol such as REST, with a token that belongs to a service user.

## What is relevant for my work

- **The only integration point with the LMS.** All reading and writing between my application and Moodle goes through these functions, not through Moodle's database. Direct database access would bypass Moodle's permission checks and break on upgrades.
- **Functions I expect to use:** `core_user_get_users_by_field` and `core_user_create_users` (find or create the trainee's account), `enrol_manual_enrol_users` (enroll in a course), `core_completion_get_activities_completion_status` (progress on course materials), `mod_quiz_get_user_attempts` (practice quizzes) and `gradereport_user_get_grade_items` (grades). The final list, with the Moodle version tested, goes into the implementation chapter.
- **Least privilege.** A dedicated service user with only the capabilities these functions need, and a token restricted to this one service.
- **Call style.** One endpoint with the function name as a parameter, so RPC over HTTP rather than resource-oriented REST (see fielding2000). Changes in Moodle are found by scheduled polling (see hohpe2003).

## Limitations

Documentation, not a scientific source. Available functions depend on the Moodle version.
