# hohpe2003: Enterprise Integration Patterns

- **Reference:** Hohpe, G., & Woolf, B. (2003). *Enterprise Integration Patterns: Designing, Building, and Deploying Messaging Solutions*. Addison-Wesley.
- **Full text:** book, not redistributable. Pattern summaries are published by the authors at https://www.enterpriseintegrationpatterns.com/
- **Topic:** System integration
- **Thesis chapters:** 2 (Background), 3 (Architecture)

## What it is

A catalog of patterns for connecting independent applications. It starts from four integration styles (File Transfer, Shared Database, Remote Procedure Invocation, Messaging) and then describes patterns for channels, routing, transformation and endpoints.

## What is relevant for my work

- **Integration styles.** The external systems cannot share a database with my application. What remains is API calls (Remote Procedure Invocation), event notifications pushed over HTTP (webhooks, a lightweight form of messaging) and, as a fallback for any system without a usable API, File Transfer (CSV exports).
- **Canonical Data Model.** The unified PostgreSQL model is a canonical model: each external system gets one translator to and from it, instead of point-to-point mappings between every pair of systems.
- **Message Translator and Content Enricher** describe converting a CRM record or a Zoom participant report into my internal entities, and adding context the source does not have (for example the cohort a meeting belongs to).
- **Polling Consumer vs Event-Driven Consumer.** Zoom and the exam platform can push webhooks. Moodle can also emit events, but only through additional plugins; to keep the LMS unmodified, I poll its standard web services on a schedule instead. Whether the CRM is polled or pushes changes depends on what its API offers (see minicrm_api). The book explains the trade-off: lower latency for events, simpler and more robust recovery for polling.
- **Idempotent Receiver.** Webhooks can be delivered more than once, and a polling run can overlap with a webhook for the same event. I will (1) store the delivery or event identifier of every processed webhook and skip repeats, and (2) write imported data with upserts on composite natural keys, for example (source system, external ID), or (meeting instance, participant, join time) for one attendance interval. A key on the external ID alone is not enough: Zoom reuses the same meeting ID for every occurrence of a recurring meeting, and one participant can join and leave several times in one session.

## Limitations

The book assumes message brokers (queues), which would be over-engineering at this scale. I use the patterns, not the broker infrastructure.
