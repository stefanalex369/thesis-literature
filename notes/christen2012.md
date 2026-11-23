# christen2012: Data Matching

- **Reference:** Christen, P. (2012). *Data Matching: Concepts and Techniques for Record Linkage, Entity Resolution, and Duplicate Detection*. Springer.
- **Full text:** book, not redistributable. DOI: https://doi.org/10.1007/978-3-642-31164-2
- **Topic:** Record linkage at small scale
- **Thesis chapter:** 4 (Unified data model and identity matching)

## What it is

A textbook on matching records that refer to the same person or entity: data cleaning and standardization, indexing, field comparison with string similarity measures, classification of record pairs, and manual review of uncertain pairs.

## What is relevant for my work

- **Standardizing names before comparing them.** Zoom display names have to be normalized: lowercase, Romanian diacritics removed (ă, â, î, ș, ț, including the older cedilla forms ş and ţ), extra whitespace and device names removed, and both "First Last" and "Last First" orders considered.
- **String similarity measures.** For names, Jaro-Winkler or a token-based measure that ignores word order; exact comparison for normalized e-mail addresses. I will choose the threshold on real data and report the result.
- **Three outcomes instead of two.** Classical record linkage sorts pairs into match, non-match and possible match. Possible matches (a first name only, a name close to two trainees, a device name such as "iPhone") go to a review list in the application where staff confirm or reject the link. Linking them automatically would silently corrupt attendance records.
- **Measuring match quality.** Precision and recall of the automatic links, measured on a manually checked sample, are the evaluation metrics for this part of the thesis.

## Limitations

General textbook; the Romanian-specific normalization rules are my own and will be described as such.
