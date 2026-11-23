# halevy2006: Data Integration: The Teenage Years

- **Reference:** Halevy, A., Rajaraman, A., & Ordille, J. (2006). Data Integration: The Teenage Years. In *Proceedings of VLDB 2006*, pp. 9–16.
- **Full text:** [`pdfs/halevy2006.pdf`](../pdfs/halevy2006.pdf) (VLDB proceedings, open)
- **Topic:** Data integration theory
- **Thesis chapter:** 2 (Background)

## What it is

A ten-year retrospective on data integration research. It explains answering queries over autonomous, heterogeneous sources through a mediated (global) schema and schema mappings, and compares the two classic ways of writing those mappings, Global-as-View (GAV) and Local-as-View (LAV). It also covers schema-mapping generation, adaptive query processing, model management and the role of AI.

## What is relevant for my work

- **Problem definition.** My case is a small instance of the problem the paper describes: several autonomous sources (CRM, LMS, videoconferencing, exam platform) with different schemas and no shared identifiers.
- **Virtual vs materialized integration.** This is the main reason I use the paper. The systems it describes keep the data in the sources and rewrite each query at run time into queries against them (virtual integration). My application does the opposite: it extracts data from the source APIs, transforms and deduplicates it, and stores it in PostgreSQL (materialized integration, the ETL approach described in vassiliadis2009). I choose this because the source APIs are rate-limited, not designed for analytical queries, and do not keep history in the form the reports need.
- **Terminology.** My unified schema plays the role of the global schema, and each import routine defines a global table in terms of source fields, which resembles GAV. I will present this only as an analogy: formally, GAV and LAV are about query reformulation over a virtual schema, which my application does not do.

## Limitations

Written in 2006 and research-oriented (XML, peer-to-peer data management). I use it for concepts and terminology, not for technology choices.
