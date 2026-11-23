# dragoni2017: Microservices: Yesterday, Today, and Tomorrow

- **Reference:** Dragoni, N., Giallorenzo, S., Lluch Lafuente, A., Mazzara, M., Montesi, F., Mustafin, R., & Safina, L. (2017). Microservices: Yesterday, Today, and Tomorrow. In *Present and Ulterior Software Engineering*, Springer, pp. 195–216.
- **Full text:** [`pdfs/dragoni2017.pdf`](../pdfs/dragoni2017.pdf) (author preprint, arXiv:1606.04036)
- **Topic:** Software architecture
- **Thesis chapter:** 3 (Architecture)

## What it is

A survey of the path from monoliths and service-oriented computing to microservices. It defines a monolith as an application whose modules cannot be executed independently, lists six problems of monoliths (labeled I|1 to I|6), and discusses microservices in terms of team organization, automation, choreography vs orchestration, dependability and security.

## What is relevant for my work

- **Definitions (section 1).** Precise definitions of monolith and microservice that I can cite instead of informal ones.
- **Arguments for the architecture decision.** The problems listed for monoliths (I|1 maintenance of large code bases, I|3 redeploying everything for one change, I|5 scaling only a stressed part, I|6 technology lock-in) appear mainly in large systems built by several teams. My application has one developer and modest load, so these problems carry little weight, while the costs of microservices described in section 4 (more network boundaries to secure and keep reliable) apply in full. This supports a single deployable application. The design I choose within it, a modular monolith, is described in newman2021, not in this paper.

## Limitations

A survey and position paper without quantitative comparisons. I use it for definitions and qualitative arguments.
