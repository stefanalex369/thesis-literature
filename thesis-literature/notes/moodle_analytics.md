# moodle_analytics: Moodle Analytics API

- **Reference:** Moodle Pty Ltd. *Analytics API*. Moodle Developer Resources. Accessed 2026-11-23.
- **Full text:** web documentation at https://moodledev.io/docs/apis/subsystems/analytics
- **Topic:** Platform documentation (LMS analytics)
- **Thesis chapter:** 6 (Reporting and learning analytics)

## What it is

Developer documentation of Moodle's built-in analytics framework: how the analyzed elements, indicators, targets and predictive models are defined inside Moodle.

## What is relevant for my work

- **The baseline.** Together with monllao2019, it describes what Moodle can do on its own. The reporting chapter starts from this baseline and explains what is missing for my case: data from outside Moodle (attendance, exam results, CRM context).
- **Indicators as a structure.** Moodle's "indicators" (calculated features of a learner's activity) are a good model for organizing the metrics in my own reports.
- **No plugin development.** Instead of extending Moodle with plugins, my application reads Moodle data through web services and combines it outside the LMS, which keeps Moodle standard and easy to upgrade.

## Limitations

Developer documentation; it does not evaluate the accuracy of the built-in models.
