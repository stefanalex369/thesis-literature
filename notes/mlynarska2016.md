# mlynarska2016: Indicators of Good Student Performance in Moodle Activity Data

- **Reference:** Młynarska, E., Greene, D., & Cunningham, P. (2016). *Indicators of Good Student Performance in Moodle Activity Data*. arXiv:1601.02975.
- **Full text:** [`pdfs/mlynarska2016.pdf`](../pdfs/mlynarska2016.pdf) (arXiv; marked by the authors as a short version)
- **Topic:** Moodle activity data and performance
- **Thesis chapter:** 6 (Reporting and learning analytics)

## What it is

A short study of Moodle data from University College Dublin (360 courses, 2,194 assignments, 71,077 submissions, anonymized before analysis). It tests three hypotheses: early submission predicts good grades, high Moodle activity before submission predicts good grades, and evening activity is more predictive than daytime activity.

## What is relevant for my work

- **Same platform.** The indicators come from data Moodle records as standard. It is a useful check that activity-based reporting on Moodle is feasible, but my application reads Moodle through web services, which return completion status, grades and quiz attempts rather than raw log rows. Indicators that need the full click log would require a Moodle report export or plugin, which is outside my scope.
- **Which indicators transfer.** "Time before deadline" applies only where a course has assignments with deadlines, which is not the case in most short courses. The general finding, that the timing and amount of activity relate to results, is what I carry over, using completion dates and quiz attempts.
- **Counter-examples.** The authors found assignments where high activity went with low grades (effort not rewarded). High activity can also signal difficulty, which is why my reports present activity as context, not as a score.
- **Small samples.** With cohorts of a few dozen trainees I will use rank correlation (Spearman) and report it per cohort with the number of trainees, rather than fit predictive models.

## Limitations

Short version of 4 pages in the arXiv form, university context. Used for concrete indicators and caveats, not as strong evidence.
