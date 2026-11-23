# monllao2019: A Quest for a One-Size-Fits-All Neural Network: Early Prediction of Students at Risk in Online Courses

- **Reference:** Monllaó Olivé, D., Huynh, D. Q., Reynolds, M., Dougiamas, M., & Wiese, D. (2019). A Quest for a One-Size-Fits-All Neural Network: Early Prediction of Students at Risk in Online Courses. *IEEE Transactions on Learning Technologies*, 12(2), 171–183.
- **Full text:** publisher version paywalled (IEEE), not included. DOI: https://doi.org/10.1109/TLT.2019.2911068
- **Topic:** Moodle's built-in predictive analytics
- **Thesis chapter:** 6 (Reporting and learning analytics)

## What it is

Research by members of the Moodle development team, including Moodle's founder Martin Dougiamas, on predicting early which students are at risk, with models meant to work across different online courses instead of being trained for each course separately. This work is connected to the analytics framework built into Moodle (see moodle_analytics).

## What is relevant for my work

- **What Moodle already does.** To show what my application adds, I first have to describe Moodle's own analytics. This paper and the Analytics API documentation describe it.
- **What my application adds is integration, not a new model.** Moodle's analytics sees only data inside Moodle. My application combines Moodle activity with attendance from live sessions, results from the separate exam platform, and CRM data such as client company and cohort. Moodle's models cannot use any of these.
- **Many short courses.** Models that generalize across courses matter in my setting, where each course runs with a small cohort and per-course models cannot be trained.

## Limitations

Focused on neural-network prediction. My thesis implements descriptive reports, so I use this paper to position my work, not to reproduce its models.
