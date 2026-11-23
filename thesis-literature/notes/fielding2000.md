# fielding2000: Architectural Styles and the Design of Network-based Software Architectures

- **Reference:** Fielding, R. T. (2000). *Architectural Styles and the Design of Network-based Software Architectures*. Doctoral dissertation, University of California, Irvine.
- **Full text:** [`pdfs/fielding2000.pdf`](../pdfs/fielding2000.pdf) (made available by the author)
- **Topic:** REST, API design
- **Thesis chapter:** 3 (Architecture and API integration)

## What it is

The dissertation that defines REST (Representational State Transfer). Section 5.1 derives REST from the "null style" by adding six constraints one at a time (client-server, stateless, cache, uniform interface, layered system, optional code-on-demand). Section 5.2 then describes the architectural elements: resources, resource identifiers, representations and the four interface constraints.

## What is relevant for my work

- **Sections 5.1.2–5.1.7** derive the constraints; 5.1.1 is the starting point and 5.1.8 the summary. I use this to judge how REST-like each API I integrate actually is. Moodle's web services expose remote functions through a single endpoint (the function name is a request parameter), which is RPC over HTTP rather than resource-oriented REST. The Zoom API is resource-oriented.
- **Statelessness (5.1.3)** means every request carries all the context the server needs, with no session state kept on the server. In the APIs I call, this is why each request carries its own credential (a static token for Moodle, an OAuth access token for Zoom, see rfc6749).
- **Uniform interface (5.1.5 and 5.2):** the four sub-constraints are identification of resources, manipulation through representations, self-descriptive messages and hypermedia as the engine of application state (HATEOAS). The internal API of my application (for example `/trainees/{id}`, `/cohorts/{id}/attendance`) will follow the first three. It will not implement HATEOAS, and I will say so explicitly rather than call the API fully RESTful.
- **Layered system (5.1.6)** describes my application's position: an intermediary layer between its own user interface and the external systems.

## Limitations

The dissertation is about architectural styles. Authentication, pagination and rate limits are not covered; I take them from the platform documentation and from rfc6749.
