# Bachelor thesis: literature

Literature collected for my bachelor thesis at the Faculty of Mathematics and Computer Science, West University of Timișoara.

- **Thesis topic:** A Web Application for the Integrated Management of Trainees in a Professional Training Organization: Interconnecting CRM, LMS and Videoconferencing Platforms
- **Advisor:** Adriana Tănasie

## The problem in short

In a professional training organization, data about the same trainee is spread across separate systems: a CRM (MiniCRM) for registrations and client companies, an LMS (Moodle) for course content and progress, a videoconferencing platform (Zoom) for live sessions, and an online exam platform (ClassMarker). The thesis designs a web application that imports data from these systems through their APIs into one PostgreSQL data model, automates enrollment and attendance tracking, gives role-based access to staff, trainers and client companies, and reports on the relation between course activity and exam results.

## Repository structure

```
references.bib   bibliographic data for all sources (BibTeX / biblatex)
notes/           one note per source: what it is, what is relevant, where I use it
pdfs/            full texts that may be redistributed (open access, author copies, public documents)
```

"Paywalled" in the table means that the publisher version is not open access and no license allows redistributing it, so the PDF is not included here. Books are in the same situation. Official standards and documentation (GDPR, RFC 6749, platform APIs) are linked to their authoritative online versions instead of copied.

## Sources by topic

| Key | Source | Full text | Chapter |
|---|---|---|---|
| **Integration and architecture** | | | |
| [fielding2000](notes/fielding2000.md) | Fielding, *Architectural Styles and the Design of Network-based Software Architectures* | [PDF](pdfs/fielding2000.pdf) | 3 |
| [hohpe2003](notes/hohpe2003.md) | Hohpe & Woolf, *Enterprise Integration Patterns: Designing, Building, and Deploying Messaging Solutions* | book | 2, 3 |
| [halevy2006](notes/halevy2006.md) | Halevy, Rajaraman & Ordille, *Data Integration: The Teenage Years* | [PDF](pdfs/halevy2006.pdf) | 2 |
| [vassiliadis2009](notes/vassiliadis2009.md) | Vassiliadis, *A Survey of Extract–Transform–Load Technology* | paywalled | 2, 4 |
| [dragoni2017](notes/dragoni2017.md) | Dragoni et al., *Microservices: Yesterday, Today, and Tomorrow* | [PDF](pdfs/dragoni2017.pdf) | 3 |
| [newman2021](notes/newman2021.md) | Newman, *Building Microservices: Designing Fine-Grained Systems* (2nd ed.) | book | 3 |
| [lti13](notes/lti13.md) | 1EdTech, *Learning Tools Interoperability Core Specification 1.3* | [online](https://www.imsglobal.org/spec/lti/v1p3/) | 2, 3 |
| **Data quality and identity matching** | | | |
| [christophides2020](notes/christophides2020.md) | Christophides et al., *An Overview of End-to-End Entity Resolution for Big Data* | [PDF](pdfs/christophides2020.pdf) | 4 |
| [christen2012](notes/christen2012.md) | Christen, *Data Matching: Concepts and Techniques for Record Linkage, Entity Resolution, and Duplicate Detection* | book | 4 |
| **Security, access control, data protection** | | | |
| [ferraiolo1992](notes/ferraiolo1992.md) | Ferraiolo & Kuhn, *Role-Based Access Controls* | [PDF](pdfs/ferraiolo1992.pdf) | 5 |
| [sandhu1996](notes/sandhu1996.md) | Sandhu et al., *Role-Based Access Control Models* | paywalled | 5 |
| [hu2014](notes/hu2014.md) | Hu et al., *Guide to Attribute Based Access Control (ABAC) Definition and Considerations* (NIST SP 800-162) | [PDF](pdfs/hu2014.pdf) | 5 |
| [rfc6749](notes/rfc6749.md) | RFC 6749, *The OAuth 2.0 Authorization Framework* | [online](https://www.rfc-editor.org/rfc/rfc6749) | 3, 5 |
| [gdpr2016](notes/gdpr2016.md) | Regulation (EU) 2016/679, *General Data Protection Regulation* | [online](https://eur-lex.europa.eu/eli/reg/2016/679/oj) | 5, 6 |
| [owasp2025](notes/owasp2025.md) | OWASP, *OWASP Top 10:2025* | [online](https://owasp.org/Top10/2025/) | 5, 7 |
| [owaspapi2023](notes/owaspapi2023.md) | OWASP, *OWASP API Security Top 10 – 2023* | [online](https://owasp.org/API-Security/editions/2023/en/0x11-t10/) | 5, 7 |
| **Learning analytics and training evaluation** | | | |
| [ferguson2012](notes/ferguson2012.md) | Ferguson, *Learning Analytics: Drivers, Developments and Challenges* | paywalled | 6 |
| [macfadyen2010](notes/macfadyen2010.md) | Macfadyen & Dawson, *Mining LMS Data to Develop an "Early Warning System" for Educators: A Proof of Concept* | paywalled | 6 |
| [mlynarska2016](notes/mlynarska2016.md) | Młynarska, Greene & Cunningham, *Indicators of Good Student Performance in Moodle Activity Data* | [PDF](pdfs/mlynarska2016.pdf) | 6 |
| [monllao2019](notes/monllao2019.md) | Monllaó Olivé et al., *A Quest for a One-Size-Fits-All Neural Network: Early Prediction of Students at Risk in Online Courses* | paywalled | 6 |
| [hoel2018](notes/hoel2018.md) | Hoel & Chen, *Privacy and Data Protection in Learning Analytics Should Be Motivated by an Educational Maxim—Towards a Proposal* | [PDF](pdfs/hoel2018.pdf) | 5, 6 |
| [kirkpatrick2006](notes/kirkpatrick2006.md) | Kirkpatrick & Kirkpatrick, *Evaluating Training Programs: The Four Levels* (3rd ed.) | book | 6 |
| **Platform documentation** | | | |
| [moodle_external](notes/moodle_external.md) | Moodle, *External Services API* | [online](https://moodledev.io/docs/apis/subsystems/external) | 3, 7 |
| [moodle_analytics](notes/moodle_analytics.md) | Moodle, *Analytics API* | [online](https://moodledev.io/docs/apis/subsystems/analytics) | 6 |
| [zoom_api](notes/zoom_api.md) | Zoom, *API Reference, Webhooks and Server-to-Server OAuth* | [online](https://developers.zoom.us/docs/api/) | 3, 7 |
| [classmarker_api](notes/classmarker_api.md) | ClassMarker, *API and Webhooks* | [online](https://www.classmarker.com/online-testing/docs/webhooks/) | 3, 4, 7 |
| [minicrm_api](notes/minicrm_api.md) | MiniCRM, *API* | [online](https://www.minicrm.io/help/api/) | 3, 7 |

## Planned thesis structure (tentative)

1. Introduction and problem statement
2. Background: data integration and integration patterns
3. Architecture and API integration
4. Unified data model and identity matching
5. Access control, security and data protection
6. Reporting and learning analytics
7. Implementation and evaluation

The chapter numbers in the table and in the notes refer to this structure and will be updated as the thesis develops.
