# A10 Networks

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

**Areas:** Application Delivery · Load Balancing · DDoS Protection · Application Delivery Controller · Network Security · Web Application Firewall · SSL Decryption · CGNAT · Cybersecurity · Infrastructure · Kubernetes · Terraform

## A10 Networks on APIs.io

Everything profiled for A10 Networks is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/a10-networks/](https://apis.io/providers/a10-networks/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [A10 Thunder Kubernetes Connector (TKC)](https://apis.io/apis/a10-networks/thunder-kubernetes-connector/) — The Thunder Kubernetes Connector (TKC) runs inside Kubernetes and configures upstream Thunder ADC objects automatically as pods are created and scaled. It…
- [A10 Networks Authentication API](https://apis.io/apis/a10-networks/a10-networks-authentication-api/) — Session sign-on and sign-off
- [A10 Networks SLB Health Monitor API](https://apis.io/apis/a10-networks/a10-networks-slb-health-monitor-api/) — Active health probes attached to servers and service groups
- [A10 Networks SLB Server API](https://apis.io/apis/a10-networks/a10-networks-slb-server-api/) — Real backend servers
- [A10 Networks SLB Service Group API](https://apis.io/apis/a10-networks/a10-networks-slb-service-group-api/) — Service groups (pools) that bind real servers to a load-balancing method
- [A10 Networks SLB Virtual Server API](https://apis.io/apis/a10-networks/a10-networks-slb-virtual-server-api/) — Virtual servers (VIPs) that front pools of real servers

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### JSON Schema (3)

The data models the API reads and writes.

- [A10 ACOS Real Server](https://apis.io/schemas/a10-networks/a10-networks-server/)
- [A10 ACOS SLB Service Group](https://apis.io/schemas/a10-networks/a10-networks-service-group/)
- [A10 ACOS Virtual Server](https://apis.io/schemas/a10-networks/a10-networks-virtual-server/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [A10 Networks Virtual Server Structure](https://apis.io/json-structure/a10-networks/a10-networks-virtual-server-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [A10 Networks Context](https://apis.io/jsonld/a10-networks/a10-networks-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [A10 Networks Vocabulary](https://apis.io/vocabularies/a10-networks/a10-networks-vocabulary/)

#### Examples (2)

Example requests and responses.

- [A10 Networks Auth Example](https://apis.io/examples/a10-networks/a10-networks-auth-example/)
- [A10 Networks Create Virtual Server Example](https://apis.io/examples/a10-networks/a10-networks-create-virtual-server-example/)

#### Collections (5)

Postman and Open Collection request collections.

- [A10 Networks ACOS aXAPI v3 Authentication API](https://apis.io/collections/a10-networks/open-a10-networks-authentication-api/)
- [A10 Networks ACOS aXAPI v3 SLB Health Monitor API](https://apis.io/collections/a10-networks/open-a10-networks-slb-health-monitor-api/)
- [A10 Networks ACOS aXAPI v3 SLB Server API](https://apis.io/collections/a10-networks/open-a10-networks-slb-server-api/)
- [A10 Networks ACOS aXAPI v3 SLB Service Group API](https://apis.io/collections/a10-networks/open-a10-networks-slb-service-group-api/)
- [A10 Networks ACOS aXAPI v3 SLB Virtual Server API](https://apis.io/collections/a10-networks/open-a10-networks-slb-virtual-server-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [A10 Networks — jsonschema rules](https://apis.io/rules/a10-networks/a10-networks-jsonschema-spectral-rules/)
- [A10 Networks API Rules](https://apis.io/rules/a10-networks/a10-networks-rules/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [A10 Networks Domain Security](https://apis.io/security/a10-networks/a10-networks-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [A10 Networks Plans Pricing](https://apis.io/plans/a10-networks/a10-networks-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [A10 Networks Rate Limits](https://apis.io/rate-limits/a10-networks/a10-networks-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [A10 Networks Finops](https://apis.io/finops/a10-networks/a10-networks-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.a10networks.com)
- [Documentation](https://documentation.a10networks.com)
- [Support](https://support.a10networks.com)
- [Blog](https://www.a10networks.com/blog/)

## API Evangelist rating

**Kin Score 27.4** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 58.0 |
| Contract quality | 56.4 |
| Contract governance | 13.6 |
| Operational transparency | 5.3 |
| Developer ergonomics | 16.7 |
| Access clarity | 15.8 |

**Agent readiness 16.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 10.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/a10-networks/](https://apis.io/providers/a10-networks/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for A10 Networks: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/a10-networks/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
