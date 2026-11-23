# vassiliadis2009: A Survey of Extract-Transform-Load Technology

- **Reference:** Vassiliadis, P. (2009). A Survey of Extract–Transform–Load Technology. *International Journal of Data Warehousing and Mining*, 5(3), 1–27.
- **Full text:** paywalled (IGI Global), not included. DOI: https://doi.org/10.4018/jdwm.2009070101
- **Topic:** Materialized data integration
- **Thesis chapters:** 2 (Background), 4 (Data model)

## What it is

A survey of ETL (Extract-Transform-Load): the processes that extract data from operational sources, clean and transform it, and load it into a separate store for reporting, usually a data warehouse.

## What is relevant for my work

- **Name for what my import routines do.** They extract data through the source APIs, transform it into the unified model (including matching trainees across systems) and load it into PostgreSQL. This is ETL at a small scale, and it is the materialized alternative to the virtual integration described in halevy2006.
- **Staging before loading.** Keeping the raw data received from each API in a staging table before transforming it makes the imports repeatable and debuggable: when a match or a calculation is wrong, the import can be re-run from the stored raw data without calling the external API again.
- **Surrogate keys.** Internal trainee IDs are surrogate keys, independent of the IDs used by each source system. The source IDs are kept as attributes for traceability.

## Limitations

Oriented to large data warehouses and batch loading at night. My imports are smaller and more frequent, partly triggered by webhooks, so I apply the concepts, not the tooling.
