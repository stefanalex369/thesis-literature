# christophides2020: An Overview of End-to-End Entity Resolution for Big Data

- **Reference:** Christophides, V., Efthymiou, V., Palpanas, T., Papadakis, G., & Stefanidis, K. (2020). An Overview of End-to-End Entity Resolution for Big Data. *ACM Computing Surveys*, 53(6), 1–42.
- **Full text:** [`pdfs/christophides2020.pdf`](../pdfs/christophides2020.pdf) (author preprint, arXiv:1905.06397; the preprint is titled "End-to-End Entity Resolution for Big Data: A Survey")
- **Topic:** Entity resolution, data quality
- **Thesis chapter:** 4 (Unified data model and identity matching)

## What it is

A survey of entity resolution (ER): identifying different descriptions of the same real-world entity when no shared identifier exists. It organizes ER as a four-stage workflow (blocking, block processing, matching, clustering) and distinguishes Dirty ER (duplicates within one collection) from Clean-Clean ER (linking two collections that are each free of duplicates).

## What is relevant for my work

- **The central data problem of my application.** The same trainee appears in the CRM, in Moodle, in Zoom participant reports and in the exam platform, with no common ID. The introduction lists the quality problems of data integrated from internal sources such as CRMs: incompleteness, redundancy, inconsistency and incorrectness. I will use these four categories to classify the errors found in the evaluation.
- **Terminology for the two steps.** Duplicates inside the CRM are a Dirty ER problem and have to be resolved first; only then is linking the CRM with the other systems a Clean-Clean ER problem.
- **Workflow, simplified.** Of the four stages, blocking reduces to a database filter in my case (only trainees enrolled in the cohort a meeting belongs to are candidates), block processing is unnecessary at this size, and matching and clustering remain. The matching rules themselves come from christen2012.

## Limitations

The survey targets Big Data (millions of records, Web knowledge bases, distributed processing). For matching a few dozen trainees per cohort I need classical record-linkage techniques, which christen2012 covers in detail.
