# newman2021: Building Microservices (2nd edition)

- **Reference:** Newman, S. (2021). *Building Microservices: Designing Fine-Grained Systems* (2nd ed.). O'Reilly Media.
- **Full text:** book, not redistributable
- **Topic:** Software architecture
- **Thesis chapter:** 3 (Architecture)

## What it is

A practitioner book on designing and running microservices. Its first chapter compares microservices with monolithic alternatives, including the modular monolith: one deployable unit whose code is split into modules with clear boundaries.

## What is relevant for my work

- **The modular monolith as a named design.** My application will be one deployable unit with separate modules per external system (CRM, LMS, videoconferencing, exams) and per function (management, reporting). This book is the source for that design; dragoni2017 provides the definitions and the general arguments.
- **Runtime isolation inside one application.** Separate modules in the code do not stop one slow external API from blocking the whole application. I will run the synchronization jobs as background workers outside the web request path, with a timeout and a retry limit per integration and a separate database transaction per import, so that an outage of one external system only delays its own data.
- **Path to splitting later.** If an integration ever needs to be deployed separately, well-defined module boundaries are what makes that possible. This is a reason to keep the boundaries strict even in a monolith.

## Limitations

Practitioner literature rather than peer-reviewed research. I use it for a design pattern and its trade-offs, not as evidence.
