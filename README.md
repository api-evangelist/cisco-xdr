# Cisco XDR

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

Cisco XDR is Cisco's extended detection and response platform, the successor to SecureX. It correlates telemetry from Cisco Secure Endpoint, Secure Firewall, Umbrella, Duo, Secure Email and third-party sources into incidents, and exposes four distinct REST API families behind a single OAuth 2.0 authorization server: the IROH platform (inspect, enrich, response actions, integration modules, events, webhooks) at visibility.amp.cisco.com, the CTIA private-intelligence store at private.intel.amp.cisco.com, the Conure v2 incidents and investigations service at conure.us.security.cisco.com, and the Automation workflow engine at automate.us.security.cisco.com. All four publish anonymously fetchable machine-readable contracts — 52 documents, 581 operations, 1,176 schema definitions — and Cisco additionally ships a 27-tool MCP server through CiscoDevNet, stdio-only. There is no sandbox, no test mode and no idempotency key anywhere, including on the operation that blocks, isolates and quarantines.

**Areas:** Security · XDR · Threat Detection · Incident Response · SOC · Threat Intelligence · Extended Detection and Response · Authentication · Webhook · Automation · MCP

## Cisco XDR on APIs.io

Everything profiled for Cisco XDR is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cisco-xdr/](https://apis.io/providers/cisco-xdr/)** — or go straight to one of the APIs or properties below.

### APIs (89)

- [Cisco XDR Actor API](https://apis.io/apis/cisco-xdr/cisco-xdr-actor-api/) — Actor operations
- [Cisco XDR Asset API](https://apis.io/apis/cisco-xdr/cisco-xdr-asset-api/) — Asset operations
- [Cisco XDR Asset Mapping API](https://apis.io/apis/cisco-xdr/cisco-xdr-asset-mapping-api/) — Asset Mapping operations
- [Cisco XDR Asset Properties API](https://apis.io/apis/cisco-xdr/cisco-xdr-asset-properties-api/) — Asset Properties operations
- [Cisco XDR Attack Pattern API](https://apis.io/apis/cisco-xdr/cisco-xdr-attack-pattern-api/) — Attack Pattern operations
- [Cisco XDR Bulk API](https://apis.io/apis/cisco-xdr/cisco-xdr-bulk-api/) — The Bulk API from Cisco XDR — 1 operation(s) for bulk.
- [Cisco XDR Bundle API](https://apis.io/apis/cisco-xdr/cisco-xdr-bundle-api/) — The Bundle API from Cisco XDR — 2 operation(s) for bundle.
- [Cisco XDR Campaign API](https://apis.io/apis/cisco-xdr/cisco-xdr-campaign-api/) — Campaign operations
- [Cisco XDR Casebook API](https://apis.io/apis/cisco-xdr/cisco-xdr-casebook-api/) — Casebook operations
- [Cisco XDR COA API](https://apis.io/apis/cisco-xdr/cisco-xdr-coa-api/) — COA operations
- [Cisco XDR Deliberate API](https://apis.io/apis/cisco-xdr/cisco-xdr-deliberate-api/) — This set of routes allow to quickly get answers from your integrations You might use them at the start of any investigation to quickly get answers from your…
- [Cisco XDR Event API](https://apis.io/apis/cisco-xdr/cisco-xdr-event-api/) — Events operations
- [Cisco XDR Feed API](https://apis.io/apis/cisco-xdr/cisco-xdr-feed-api/) — Feed operations
- [Cisco XDR Feedback API](https://apis.io/apis/cisco-xdr/cisco-xdr-feedback-api/) — Feedback Routes
- [Cisco XDR Health API](https://apis.io/apis/cisco-xdr/cisco-xdr-health-api/) — This set of routes allow to check the health of your integrations setup Verify if your modules are setup correctly and if your credentials are correct.
- [Cisco XDR Incident API](https://apis.io/apis/cisco-xdr/cisco-xdr-incident-api/) — Incident operations
- [Cisco XDR Indicator API](https://apis.io/apis/cisco-xdr/cisco-xdr-indicator-api/) — Indicator operations
- [Cisco XDR Inspect API](https://apis.io/apis/cisco-xdr/cisco-xdr-inspect-api/) — Inspect related routes
- [Cisco XDR Investigation API](https://apis.io/apis/cisco-xdr/cisco-xdr-investigation-api/) — The Investigation API from Cisco XDR — 8 operation(s) for investigation.
- [Cisco XDR INVITE API](https://apis.io/apis/cisco-xdr/cisco-xdr-invite-api/) — The INVITE API from Cisco XDR — 2 operation(s) for invite.
- [Cisco XDR Iroh API](https://apis.io/apis/cisco-xdr/cisco-xdr-iroh-api/) — The Iroh API from Cisco XDR — 3 operation(s) for iroh.
- [Cisco XDR Judgement API](https://apis.io/apis/cisco-xdr/cisco-xdr-judgement-api/) — Judgement operations
- [Cisco XDR LOGIN API](https://apis.io/apis/cisco-xdr/cisco-xdr-login-api/) — The LOGIN API from Cisco XDR — 4 operation(s) for login.
- [Cisco XDR Malware API](https://apis.io/apis/cisco-xdr/cisco-xdr-malware-api/) — Malware operations
- [Cisco XDR Metrics API](https://apis.io/apis/cisco-xdr/cisco-xdr-metrics-api/) — The Metrics API from Cisco XDR — 1 operation(s) for metrics.
- [Cisco XDR Module Instance API](https://apis.io/apis/cisco-xdr/cisco-xdr-moduleinstance-api/) — ModuleInstance Routes
- [Cisco XDR Module Type API](https://apis.io/apis/cisco-xdr/cisco-xdr-moduletype-api/) — ModuleType Routes
- [Cisco XDR Module Type Patch API](https://apis.io/apis/cisco-xdr/cisco-xdr-moduletypepatch-api/) — ModuleTypePatch Routes
- [Cisco XDR Note API](https://apis.io/apis/cisco-xdr/cisco-xdr-note-api/) — The Note API from Cisco XDR — 8 operation(s) for note.
- [Cisco XDR Observe API](https://apis.io/apis/cisco-xdr/cisco-xdr-observe-api/) — This set of routes allow to get in depth investigation data about a threat You might use them at the start of any investigation to get the full picture and…
- [Cisco XDR One Click API](https://apis.io/apis/cisco-xdr/cisco-xdr-one-click-api/) — One-click Routes
- [Cisco XDR Private Intel API](https://apis.io/apis/cisco-xdr/cisco-xdr-private-intel-api/) — Access private-intel
- [Cisco XDR Properties API](https://apis.io/apis/cisco-xdr/cisco-xdr-properties-api/) — The Properties API from Cisco XDR — 1 operation(s) for properties.
- [Cisco XDR Query API](https://apis.io/apis/cisco-xdr/cisco-xdr-query-api/) — This set of routes allow to query for records related to observable events.Results are returned in OCSF format.
- [Cisco XDR Refer API](https://apis.io/apis/cisco-xdr/cisco-xdr-refer-api/) — This set of routes allow to get relevant Reference links and quickly pivot pursuing your investigation on a specific product interface.
- [Cisco XDR Relationship API](https://apis.io/apis/cisco-xdr/cisco-xdr-relationship-api/) — Relationship operations
- [Cisco XDR Reputation API](https://apis.io/apis/cisco-xdr/cisco-xdr-reputation-api/) — The Reputation API from Cisco XDR — 1 operation(s) for reputation.
- [Cisco XDR Response API](https://apis.io/apis/cisco-xdr/cisco-xdr-response-api/) — IROH Response
- [Cisco XDR Session Cookie API](https://apis.io/apis/cisco-xdr/cisco-xdr-session-cookie-api/) — Cookie-based session validation
- [Cisco XDR Sighting API](https://apis.io/apis/cisco-xdr/cisco-xdr-sighting-api/) — Sighting operations
- [Cisco XDR Status API](https://apis.io/apis/cisco-xdr/cisco-xdr-status-api/) — The Status API from Cisco XDR — 1 operation(s) for status.
- [Cisco XDR Target Record API](https://apis.io/apis/cisco-xdr/cisco-xdr-target-record-api/) — Target Record operations
- [Cisco XDR Tool API](https://apis.io/apis/cisco-xdr/cisco-xdr-tool-api/) — Tool operations
- [Cisco XDR Verdict API](https://apis.io/apis/cisco-xdr/cisco-xdr-verdict-api/) — The Verdict API from Cisco XDR — 1 operation(s) for verdict.
- [Cisco XDR Version API](https://apis.io/apis/cisco-xdr/cisco-xdr-version-api/) — The Version API from Cisco XDR — 1 operation(s) for version.
- [Cisco XDR Vulnerability API](https://apis.io/apis/cisco-xdr/cisco-xdr-vulnerability-api/) — The Vulnerability API from Cisco XDR — 9 operation(s) for vulnerability.
- [Cisco XDR Webhook API](https://apis.io/apis/cisco-xdr/cisco-xdr-webhook-api/) — Webhook Routes
- [Cisco XDR Webhook Result API](https://apis.io/apis/cisco-xdr/cisco-xdr-webhookresult-api/) — The WebhookResult API from Cisco XDR — 2 operation(s) for webhookresult.
- [Cisco XDR MCP Server](https://apis.io/apis/cisco-xdr/cisco-xdr-mcp-server/) — Model Context Protocol server published by CiscoDevNet exposing 27 Cisco XDR tools across Inspect, Investigate, Incidents, Response Actions, Casebooks,…
- [Cisco XDR Calendars API](https://apis.io/apis/cisco-xdr/cisco-xdr-calendars-api/) — The Calendars API from Cisco XDR — 3 operation(s) for calendars.
- [Cisco XDR Categories API](https://apis.io/apis/cisco-xdr/cisco-xdr-categories-api/) — The Categories API from Cisco XDR — 2 operation(s) for categories.
- [Cisco XDR Change Owner API](https://apis.io/apis/cisco-xdr/cisco-xdr-changeowner-api/) — The ChangeOwner API from Cisco XDR — 1 operation(s) for changeowner.
- [Cisco XDR Comments API](https://apis.io/apis/cisco-xdr/cisco-xdr-comments-api/) — The Comments API from Cisco XDR — 2 operation(s) for comments.
- [Cisco XDR Events API](https://apis.io/apis/cisco-xdr/cisco-xdr-events-api/) — The Events API from Cisco XDR — 2 operation(s) for events.
- [Cisco XDR Events Rate Limit API](https://apis.io/apis/cisco-xdr/cisco-xdr-eventsratelimit-api/) — The EventsRateLimit API from Cisco XDR — 1 operation(s) for eventsratelimit.
- [Cisco XDR Metadata API](https://apis.io/apis/cisco-xdr/cisco-xdr-metadata-api/) — The Metadata API from Cisco XDR — 1 operation(s) for metadata.
- [Cisco XDR Ratings API](https://apis.io/apis/cisco-xdr/cisco-xdr-ratings-api/) — The Ratings API from Cisco XDR — 3 operation(s) for ratings.
- [Cisco XDR References API](https://apis.io/apis/cisco-xdr/cisco-xdr-references-api/) — The References API from Cisco XDR — 1 operation(s) for references.
- [Cisco XDR Remote Meta API](https://apis.io/apis/cisco-xdr/cisco-xdr-remotemeta-api/) — The RemoteMeta API from Cisco XDR — 3 operation(s) for remotemeta.
- [Cisco XDR Rules API](https://apis.io/apis/cisco-xdr/cisco-xdr-rules-api/) — The Rules API from Cisco XDR — 4 operation(s) for rules.
- [Cisco XDR Runtime Users API](https://apis.io/apis/cisco-xdr/cisco-xdr-runtimeusers-api/) — The RuntimeUsers API from Cisco XDR — 2 operation(s) for runtimeusers.
- [Cisco XDR Schedules API](https://apis.io/apis/cisco-xdr/cisco-xdr-schedules-api/) — The Schedules API from Cisco XDR — 2 operation(s) for schedules.
- [Cisco XDR Schemas API](https://apis.io/apis/cisco-xdr/cisco-xdr-schemas-api/) — The Schemas API from Cisco XDR — 2 operation(s) for schemas.
- [Cisco XDR Share Object Permissions API](https://apis.io/apis/cisco-xdr/cisco-xdr-shareobjectpermissions-api/) — The ShareObjectPermissions API from Cisco XDR — 1 operation(s) for shareobjectpermissions.
- [Cisco XDR SXIROH Incident API](https://apis.io/apis/cisco-xdr/cisco-xdr-sxirohincident-api/) — The SXIROHIncident API from Cisco XDR — 1 operation(s) for sxirohincident.
- [Cisco XDR Tables API](https://apis.io/apis/cisco-xdr/cisco-xdr-tables-api/) — The Tables API from Cisco XDR — 2 operation(s) for tables.
- [Cisco XDR Table Types API](https://apis.io/apis/cisco-xdr/cisco-xdr-tabletypes-api/) — The TableTypes API from Cisco XDR — 2 operation(s) for tabletypes.
- [Cisco XDR Targets API](https://apis.io/apis/cisco-xdr/cisco-xdr-targets-api/) — The Targets API from Cisco XDR — 3 operation(s) for targets.
- [Cisco XDR Tasks API](https://apis.io/apis/cisco-xdr/cisco-xdr-tasks-api/) — The Tasks API from Cisco XDR — 5 operation(s) for tasks.
- [Cisco XDR Tenants API](https://apis.io/apis/cisco-xdr/cisco-xdr-tenants-api/) — The Tenants API from Cisco XDR — 3 operation(s) for tenants.
- [Cisco XDR Triggers API](https://apis.io/apis/cisco-xdr/cisco-xdr-triggers-api/) — The Triggers API from Cisco XDR — 2 operation(s) for triggers.
- [Cisco XDR Variables API](https://apis.io/apis/cisco-xdr/cisco-xdr-variables-api/) — The Variables API from Cisco XDR — 3 operation(s) for variables.
- [Cisco XDR Variable Types API](https://apis.io/apis/cisco-xdr/cisco-xdr-variabletypes-api/) — The VariableTypes API from Cisco XDR — 3 operation(s) for variabletypes.
- [Cisco XDR Webhooks API](https://apis.io/apis/cisco-xdr/cisco-xdr-webhooks-api/) — The Webhooks API from Cisco XDR — 3 operation(s) for webhooks.
- [Cisco XDR Workflows API](https://apis.io/apis/cisco-xdr/cisco-xdr-workflows-api/) — The Workflows API from Cisco XDR — 20 operation(s) for workflows.
- [Cisco XDR Workflow Variable References API](https://apis.io/apis/cisco-xdr/cisco-xdr-workflowvariablereferences-api/) — The WorkflowVariableReferences API from Cisco XDR — 1 operation(s) for workflowvariablereferences.
- [Cisco XDR Xchange API](https://apis.io/apis/cisco-xdr/cisco-xdr-xchange-api/) — The Xchange API from Cisco XDR — 4 operation(s) for xchange.
- [Cisco XDR Incident Overview API](https://apis.io/apis/cisco-xdr/cisco-xdr-incident-overview-api/) — The Incident Overview API from Cisco XDR — 16 operation(s) for incident overview.
- [Cisco XDR Incident Report API](https://apis.io/apis/cisco-xdr/cisco-xdr-incident-report-api/) — The Incident Report API from Cisco XDR — 3 operation(s) for incident report.
- [Cisco XDR Incident Routes using Entities API](https://apis.io/apis/cisco-xdr/cisco-xdr-incident-routes-using-entities-api/) — The Incident Routes using Entities API from Cisco XDR — 5 operation(s) for incident routes using entities.
- [Cisco XDR Incident Summary API](https://apis.io/apis/cisco-xdr/cisco-xdr-incident-summary-api/) — The Incident Summary API from Cisco XDR — 1 operation(s) for incident summary.
- [Cisco XDR Investigation Creation API](https://apis.io/apis/cisco-xdr/cisco-xdr-investigation-creation-api/) — The Investigation Creation API from Cisco XDR — 4 operation(s) for investigation creation.
- [Cisco XDR Investigation Data API](https://apis.io/apis/cisco-xdr/cisco-xdr-investigation-data-api/) — The Investigation Data API from Cisco XDR — 11 operation(s) for investigation data.
- [Cisco XDR Investigation Routes using Entities API](https://apis.io/apis/cisco-xdr/cisco-xdr-investigation-routes-using-entities-api/) — The Investigation Routes using Entities API from Cisco XDR — 3 operation(s) for investigation routes using entities.
- [Cisco XDR Investigation Save/Update API](https://apis.io/apis/cisco-xdr/cisco-xdr-investigation-save-update-api/) — The Investigation Save/Update API from Cisco XDR — 8 operation(s) for investigation save/update.
- [Cisco XDR Report API](https://apis.io/apis/cisco-xdr/cisco-xdr-report-api/) — The Report API from Cisco XDR — 13 operation(s) for report.
- [Cisco XDR Graph QL API](https://apis.io/apis/cisco-xdr/cisco-xdr-graph-ql-api/) — The Graph QL API from Cisco XDR — 1 operation(s) for graph ql.
- [Cisco XDR Target Groups API](https://apis.io/apis/cisco-xdr/cisco-xdr-target-groups-api/) — The Target Groups API from Cisco XDR — 2 operation(s) for target groups.
- [Cisco XDR Workflow Instances API](https://apis.io/apis/cisco-xdr/cisco-xdr-workflow-instances-api/) — The Workflow Instances API from Cisco XDR — 7 operation(s) for workflow instances.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Cisco Xdr Webhooks](https://apis.io/asyncapis/cisco-xdr/cisco-xdr-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [cisco-xdr](https://apis.io/servers/cisco-xdr/cisco-xdr/)

#### Overlays (4)

OpenAPI overlays, including conversational phrasing for each operation.

- [Cisco Xdr Automation Overlay](https://apis.io/overlays/cisco-xdr/cisco-xdr-automation-overlay/)
- [Cisco Xdr Incidents Investigations Overlay](https://apis.io/overlays/cisco-xdr/cisco-xdr-incidents-investigations-overlay/)
- [Cisco Xdr Inspect Overlay](https://apis.io/overlays/cisco-xdr/cisco-xdr-inspect-overlay/)
- [Cisco Xdr Iroh Response Overlay](https://apis.io/overlays/cisco-xdr/cisco-xdr-iroh-response-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Cisco Xdr Authentication](https://apis.io/security/cisco-xdr/cisco-xdr-authentication/)
- [Cisco Xdr Domain Security](https://apis.io/security/cisco-xdr/cisco-xdr-domain-security/)
- [Cisco Xdr Trust Center](https://apis.io/security/cisco-xdr/cisco-xdr-trust-center/)
- [Cisco Xdr Vulnerability Disclosure](https://apis.io/security/cisco-xdr/cisco-xdr-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Cisco Xdr Scopes](https://apis.io/scopes/cisco-xdr/cisco-xdr-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cisco Xdr Plans Pricing](https://apis.io/plans/cisco-xdr/cisco-xdr-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cisco Xdr Rate Limits](https://apis.io/rate-limits/cisco-xdr/cisco-xdr-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cisco.com/site/us/en/products/security/xdr/index.html)
- [Documentation](https://developer.cisco.com/docs/cisco-xdr/)
- [Getting started](https://developer.cisco.com/docs/cisco-xdr/getting-started/)
- [API reference](https://developer.cisco.com/docs/cisco-xdr/)
- [Pricing](https://www.cisco.com/site/us/en/products/security/xdr/index.html)
- [Support](https://developer.cisco.com/docs/cisco-xdr/developer-support/)
- [Changelog](https://developer.cisco.com/docs/cisco-xdr/api-changelog/)
- [Blog](https://blogs.cisco.com/tag/xdr)
- [Security](https://sec.cloudapps.cisco.com/security/center/resources/security_vulnerability_policy.html)
- [Compliance](https://trustportal.cisco.com/)
- [Terms of service](https://www.cisco.com/c/en/us/about/legal/cloud-and-software.html)
- [Privacy policy](https://www.cisco.com/c/en/us/about/legal/privacy-full.html)
- [GitHub](https://github.com/CiscoDevNet)
- [Status](https://status.tdr.cisco.com/)

## API Evangelist rating

**Kin Score 68.3** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 70.0 |
| Contract quality | 55.8 |
| Contract governance | 4.5 |
| Operational transparency | 76.3 |
| Developer ergonomics | 66.1 |
| Access clarity | 85.5 |

**Agent readiness 39.1** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | yes |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | mostly |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cisco-xdr/](https://apis.io/providers/cisco-xdr/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cisco XDR: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cisco-xdr/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
