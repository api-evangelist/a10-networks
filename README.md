# A10 Networks (a10-networks)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

A10 Networks (NYSE: ATEN) is a San Jose, California–headquartered application delivery and cybersecurity company founded in 2004 by Lee Chen. A10 builds the ACOS (Application Centric Operating System) software platform that powers its Thunder family of physical appliances, virtual machines (vThunder), and containerized form factors across hyperscalers and private clouds. The product line spans the Thunder ADC (Application Delivery Controller for L4–L7 server load balancing and GSLB), the Thunder TPS / A10 Defend portfolio (DDoS detection, mitigation, orchestration, and Threat Control SaaS) protecting service-provider and enterprise networks from volumetric and application-layer attacks, Thunder CGN (Carrier-Grade NAT and IPv4/IPv6 transition), Thunder CFW (consolidated firewall, VPN, CGN, and secure web gateway), SSL Insight for encrypted traffic decryption, the A10 Defend Next-Gen WAF (incorporating ThreatX), and the A10 AI Firewall for protecting LLM and AI application traffic. Every ACOS device exposes the aXAPI v3 — a RESTful HTTPS interface that is the primary configuration and operational control plane for the platform, supporting ACOS 4.0.0 through 7.0.2. The aXAPI surface is exhaustive (the official Terraform provider exposes 3,627 resources) and is wrapped by official Ansible collections (a10-acos-axapi, a10-acos-cli), a Python client (acos-client), the Thunder Kubernetes Connector (TKC, with 24 CRDs for pod-driven VIP automation), and integrations for OpenStack Octavia, Neutron LBaaS, AWS CloudFormation, Azure ARM, VMware vSphere, Helm, and Prometheus. A10 reported record annual revenue of $290.6M in FY2025 (up 11.0% year over year) under CEO Dhrupad Trivedi, serving 7,700+ customers across 117 countries.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/a10-networks/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/a10-networks/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Application Delivery
- Load Balancing
- DDoS Protection
- Application Delivery Controller
- Network Security
- Web Application Firewall
- SSL Decryption
- CGNAT
- Cybersecurity
- Infrastructure
- Kubernetes
- Terraform
- Ansible
- REST API
- Networking

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### A10 Networks ACOS aXAPI v3

The ACOS aXAPI v3 is the RESTful HTTPS configuration and operational control plane for every A10 Thunder device — physical, virtual (vThunder), or containerized. It covers the full ACOS object model: Server Load Balancing (virtual servers, real servers, service groups, health monitors, SSL templates, aFleX scripts), GSLB, DDoS protection objects, CGNAT pools, system configuration, networking, routing, partitions, and operational/statistics resources. Authentication is session-based (POST /axapi/v3/auth returns a signature for the `Authorization: A10 <signature>` header). The aXAPI is the substrate under the Terraform provider, the Ansible collections, the Kubernetes Connector, and the Python acos-client.

- **Human URL:** [https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html](https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html)

#### Tags

- Application Delivery
- Load Balancing
- DDoS Protection
- SLB
- REST API
- ACOS

#### Properties

- [Documentation](https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html)
- [Documentation](https://documentation.a10networks.com/ACOS-Docs/axapi/608/index.html)
- [Blog](https://www.a10networks.com/blog/axapi-rest-based-application-programming-interface-integration/)
- [OpenAPI](openapi/a10-networks-axapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/a10-networks-virtual-server-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/a10-networks-server-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/a10-networks-service-group-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/a10-networks-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Ruleset](rules/a10-networks-rules.yml)

### A10 Thunder Kubernetes Connector (TKC)

The Thunder Kubernetes Connector (TKC) runs inside Kubernetes and configures upstream Thunder ADC objects automatically as pods are created and scaled. It defines 24 CRDs covering VirtualServer, VirtualPort, ServiceGroup, HealthMonitor, NatPool, A10IPPool, ActiveActiveHADevice, ClientSsl/ServerSsl templates, TCP/UDP/HTTP/ HTTPS templates, persistence templates, policy templates, and cipher templates — exposing the full L4–L7 ADC surface as native Kubernetes resources.

- **Human URL:** [https://github.com/a10networks/tkc-doc](https://github.com/a10networks/tkc-doc)

#### Tags

- Kubernetes
- CRD
- Cloud Native
- Application Delivery
- Service Mesh

#### Properties

- [Documentation](https://github.com/a10networks/tkc-doc)
- [Source Code](https://github.com/a10networks/tkc-doc)
- [Kubernetes C R D](crd/)

## Common Properties

- [Website](https://www.a10networks.com)
- [Products](https://www.a10networks.com/products/)
- [Documentation](https://documentation.a10networks.com)
- [a X A P I  Documentation](https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html)
- [Source Code](https://github.com/a10networks)
- [Terraform Provider](https://github.com/a10networks/terraform-provider-thunder)
- [Ansible Collection](https://github.com/a10networks/a10-acos-axapi)
- [Python Client](https://github.com/a10networks/acos-client)
- [Kubernetes Connector](https://github.com/a10networks/tkc-doc)
- [Open Stack Octavia](https://github.com/a10networks/a10-octavia)
- [Prometheus Exporter](https://github.com/a10networks/PrometheusExporter)
- [A W S Cloud Formation](https://github.com/a10networks/AWS-CFT)
- [Azure A R M Templates](https://github.com/a10networks/A10-azure-arm-templates)
- [V Mware Templates](https://github.com/a10networks/a10-vmware-templates)
- [a Fle X Scripts](https://github.com/a10networks/aflex-collection)
- [Helm Chart](https://github.com/a10networks/acos-prometheus-exporter-helm-chart)
- [Support](https://support.a10networks.com)
- [Community](https://glm.a10networks.com)
- [Blog](https://www.a10networks.com/blog/)
- [Newsroom](https://www.a10networks.com/news/)
- [Investor Relations](https://investors.a10networks.com)
- [Careers](https://www.a10networks.com/company/careers/)
- [Contact](https://www.a10networks.com/contact-us/)
- [Twitter](https://twitter.com/A10Networks)
- [LinkedIn](https://www.linkedin.com/company/a10networks)
- [YouTube](https://www.youtube.com/user/a10networks)
- [Git Hub](https://github.com/a10networks)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
