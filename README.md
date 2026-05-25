# A10 Networks (a10-networks)

A10 Networks (NYSE: ATEN) is a San Jose, California–headquartered application delivery and cybersecurity company founded in 2004 by Lee Chen. A10 builds the ACOS (Application Centric Operating System) software platform that powers its Thunder family of physical appliances, virtual machines (vThunder), and containerized form factors across hyperscalers and private clouds. The portfolio spans Thunder ADC (L4–L7 load balancing and GSLB), the A10 Defend DDoS portfolio (Detector, Mitigator, Orchestrator, Threat Control SaaS), Thunder CGN (Carrier-Grade NAT and IPv6 transition), Thunder CFW (consolidated firewall, VPN, CGN, secure web gateway), SSL Insight for encrypted-traffic decryption, the A10 Defend Next-Gen WAF (incorporating ThreatX), and the A10 AI Firewall for protecting LLM/AI application traffic. Every ACOS device exposes the **aXAPI v3** — a RESTful HTTPS interface that is the primary configuration and operational control plane, wrapped by official Terraform, Ansible, Python, and Kubernetes Connector tooling. A10 reported record annual revenue of $290.6M for FY2025 (up 11.0% YoY) under CEO Dhrupad Trivedi, serving 7,700+ customers across 117 countries.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/a10-networks/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Application Delivery, Load Balancing, DDoS Protection, Application Delivery Controller, Network Security, Web Application Firewall, SSL Decryption, CGNAT, Cybersecurity, Infrastructure, Kubernetes, Terraform, Ansible, REST API, Networking

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### A10 Networks ACOS aXAPI v3
The RESTful HTTPS configuration and operational control plane for every A10 Thunder device — physical, virtual (vThunder), or containerized. Covers the full ACOS object model: SLB (virtual servers, real servers, service groups, health monitors, SSL templates, aFleX), GSLB, DDoS protection, CGNAT pools, system, networking, routing, partitions, and operational/statistics resources. Session-based authentication via `POST /axapi/v3/auth` returning a signature for the `Authorization: A10 <signature>` header. The aXAPI is the substrate under the Terraform provider (3,627 resources), the Ansible collections, the Kubernetes Connector, and the Python `acos-client`.

**Human URL:** [https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html](https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html)

- [Documentation — ACOS 7.0.2 aXAPI v3](https://documentation.a10networks.com/ACOS-Docs/axapi/702/start_here.html)
- [Documentation — ACOS 6.0.8 aXAPI v3](https://documentation.a10networks.com/ACOS-Docs/axapi/608/index.html)
- [Blog — aXAPI REST-Based API Integration](https://www.a10networks.com/blog/axapi-rest-based-application-programming-interface-integration/)
- [OpenAPI](openapi/a10-networks-axapi-openapi.yml)
- [JSON Schema — Virtual Server](json-schema/a10-networks-virtual-server-schema.json)
- [JSON Schema — Server](json-schema/a10-networks-server-schema.json)
- [JSON Schema — Service Group](json-schema/a10-networks-service-group-schema.json)
- [JSON-LD Context](json-ld/a10-networks-context.jsonld)
- [Spectral Ruleset](rules/a10-networks-rules.yml)
- [Naftiko Capability — Virtual Servers](capabilities/slb-virtual-servers.yaml)
- [Naftiko Capability — Servers](capabilities/slb-servers.yaml)
- [Naftiko Capability — Service Groups](capabilities/slb-service-groups.yaml)
- [Naftiko Capability — Health Monitors](capabilities/slb-health-monitors.yaml)

### A10 Thunder Kubernetes Connector (TKC)
Runs inside Kubernetes and configures upstream Thunder ADC objects automatically as pods are created and scaled. Defines 24 CRDs covering the SLB and template object model — VirtualServer, VirtualPort, ServiceGroup, HealthMonitor, NatPool, A10IPPool, ActiveActiveHADevice, ClientSsl/ServerSsl, TCP/UDP/HTTP/HTTPS/cipher/persistence/policy templates — exposing the full L4–L7 ADC surface as native Kubernetes resources.

**Human URL:** [https://github.com/a10networks/tkc-doc](https://github.com/a10networks/tkc-doc)

- [Documentation](https://github.com/a10networks/tkc-doc)
- [CRDs (24 files)](crd/)

## SDKs, Tools, and Integrations

| Project | Purpose | Language | License |
|---|---|---|---|
| [terraform-provider-thunder](https://github.com/a10networks/terraform-provider-thunder) | Official Terraform provider — 3,627 ACOS resources | Go | BSD-2-Clause |
| [a10-acos-axapi](https://github.com/a10networks/a10-acos-axapi) | Official Ansible collection for the aXAPI v3 surface | Python | Apache-2.0 |
| [a10-acos-cli](https://github.com/a10networks/a10-acos-cli) | Ansible collection for CLI-based ACOS configuration | Python | Apache-2.0 |
| [acos-client](https://github.com/a10networks/acos-client) | Official Python client for the aXAPI v3 (ACOS 4.0.0+) | Python | Apache-2.0 |
| [tkc-doc](https://github.com/a10networks/tkc-doc) | Thunder Kubernetes Connector docs and CRDs | YAML | Apache-2.0 |
| [a10-octavia](https://github.com/a10networks/a10-octavia) | OpenStack Octavia provider driver | Python | Apache-2.0 |
| [a10-neutron-lbaas](https://github.com/a10networks/a10-neutron-lbaas) | OpenStack Neutron LBaaS driver | Python | Apache-2.0 |
| [AWS-CFT](https://github.com/a10networks/AWS-CFT) | AWS CloudFormation templates for vThunder | Python | Apache-2.0 |
| [A10-azure-arm-templates](https://github.com/a10networks/A10-azure-arm-templates) | Azure ARM templates for vThunder | PowerShell | Apache-2.0 |
| [a10-vmware-templates](https://github.com/a10networks/a10-vmware-templates) | VMware vSphere deployment templates | Python | Apache-2.0 |
| [PrometheusExporter](https://github.com/a10networks/PrometheusExporter) | Custom Prometheus exporter for vThunder | Python | Apache-2.0 |
| [thunder-observability-agent](https://github.com/a10networks/thunder-observability-agent) | Observability agent | — | Apache-2.0 |
| [aflex-collection](https://github.com/a10networks/aflex-collection) | aFleX (Tcl) scripts for L7 traffic manipulation | Tcl | Apache-2.0 |
| [axapi-collection](https://github.com/a10networks/axapi-collection) | Sample aXAPI scripts and integrations | Python | Apache-2.0 |
| [glm-client](https://github.com/a10networks/glm-client) | Global License Manager licensing scripts | Python | Apache-2.0 |
| [a10-nlbaas2oct](https://github.com/a10networks/a10-nlbaas2oct) | Migrate Thunder from Neutron LBaaS to Octavia | Python | Apache-2.0 |
| [a10-saltstack](https://github.com/a10networks/a10-saltstack) | SaltStack modules for Thunder | Python | Apache-2.0 |
| [acos-prometheus-exporter-helm-chart](https://github.com/a10networks/acos-prometheus-exporter-helm-chart) | Helm chart for the ACOS Prometheus exporter | HTML | Apache-2.0 |

## Commercial Surface

- [Plans & Pricing](plans/a10-networks-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/a10-networks-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/a10-networks-finops.yml) — FOCUS-aligned FinOps definition

## Vocabulary

- [Vocabulary](vocabulary/a10-networks-vocabulary.yml)
- [JSON Structure — Virtual Server](json-structure/a10-networks-virtual-server-structure.json)

## Maintainer

Kin Lane — kin@apievangelist.com
