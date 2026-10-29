# Entergram

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

Entergram is a CRM built specifically for Telegram. It connects personal Telegram accounts (not bots) into a shared team workspace where sales, support, community and trading teams manage conversations at scale — a multi-account inbox, a CRM table and Kanban pipeline, custom columns and labels, broadcast messaging, and a ticketing system with assignment, SLA and status tracking. Its developer surface has three parts: a workspace-scoped REST API (X-API-Key) covering accounts, contacts, groups, chats, messages, custom fields, tickets, webhooks and resumable events; a hosted Model Context Protocol (MCP) server for personal Telegram accounts (OAuth2 + PKCE) that lets AI agents read chats, manage tickets and update CRM fields; and outbound webhooks for incoming/outgoing message events, plus a Make.com integration.

**Areas:** Messaging · Notification · Communications · CRM · Telegram · Customer Service · Ticketing · Sales · MCP · Webhook

## Entergram on APIs.io

Everything profiled for Entergram is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/entergram/](https://apis.io/providers/entergram/)** — or go straight to one of the APIs or properties below.

### APIs (16)

- [Entergram Accounts API](https://apis.io/apis/entergram/entergram-accounts-api/) — Connected account inventory.
- [Entergram Chat Commands API](https://apis.io/apis/entergram/entergram-chat-commands-api/) — Telegram chat creation and group/channel management commands scoped to an explicit connected account.
- [Entergram Chats API](https://apis.io/apis/entergram/entergram-chats-api/) — Actor-scoped chats, linked tickets, and internal chat comments keyed by Telegram chat ID.
- [Entergram Contacts API](https://apis.io/apis/entergram/entergram-contacts-api/) — Workspace contacts deduplicated across connected accounts, including shared groups and attribution.
- [Entergram Custom Fields API](https://apis.io/apis/entergram/entergram-custom-fields-api/) — Workspace chat custom columns, ticket custom columns, selectable options, and workspace-shared chat custom field values.
- [Entergram Events API](https://apis.io/apis/entergram/entergram-events-api/) — Metadata-only, cursor-based workspace event stream for resumable integrations.
- [Entergram Groups API](https://apis.io/apis/entergram/entergram-groups-api/) — Workspace groups derived from shared-contact graph, with invite-link and member metadata when cached.
- [Entergram Live Chats API](https://apis.io/apis/entergram/entergram-live-chats-api/) — Actor-owned live Telegram transport view used for current chat discovery before message operations.
- [Entergram Make webhooks API](https://apis.io/apis/entergram/entergram-make-webhooks-api/) — The Make webhooks API from Entergram — 2 operation(s) for make webhooks.
- [Entergram Members API](https://apis.io/apis/entergram/entergram-members-api/) — Safe workspace member identity, role, permissions, and seat assignment metadata.
- [Entergram Messages API](https://apis.io/apis/entergram/entergram-messages-api/) — Telegram message history and message write operations scoped to an explicit account and chat.
- [Entergram System API](https://apis.io/apis/entergram/entergram-system-api/) — Authentication and runtime context.
- [Entergram Tickets API](https://apis.io/apis/entergram/entergram-tickets-api/) — Workspace ticket inventory, ticket detail, comments, and linked chat filters.
- [Entergram Webhooks API](https://apis.io/apis/entergram/entergram-webhooks-api/) — API-only webhook endpoint configuration, secret rotation, tests, and sanitized delivery status.
- [Entergram Workspace API](https://apis.io/apis/entergram/entergram-workspace-api/) — Workspace metadata and feature access.
- [Entergram Workspace Chats API](https://apis.io/apis/entergram/entergram-workspace-chats-api/) — Shared CRM chat view from frontend DB, deduplicated across workspace accounts and suited for metadata, custom fields, and ticket workflows.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Entergram Webhooks](https://apis.io/asyncapis/entergram/entergram-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Entergram Telegram MCP Server](https://apis.io/servers/entergram/entergram-telegram-mcp-server/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Entergram Openapi Overlay](https://apis.io/overlays/entergram/entergram-openapi-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Entergram Authentication](https://apis.io/security/entergram/entergram-authentication/)
- [Entergram Domain Security](https://apis.io/security/entergram/entergram-domain-security/)
- [Entergram Trust Center](https://apis.io/security/entergram/entergram-trust-center/)
- [Entergram Vulnerability Disclosure](https://apis.io/security/entergram/entergram-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Entergram Scopes](https://apis.io/scopes/entergram/entergram-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Entergram Plans Pricing](https://apis.io/plans/entergram/entergram-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Entergram Rate Limits](https://apis.io/rate-limits/entergram/entergram-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.entergram.com)
- [Documentation](https://api.entergram.com/docs)
- [API reference](https://api.entergram.com/docs)
- [Pricing](https://www.entergram.com/pricing)
- [Support](https://www.entergram.com/help-center)
- [Blog](https://www.entergram.com/blog)
- [Terms of service](https://www.entergram.com/terms)
- [Privacy policy](https://www.entergram.com/privacy)
- [Status](https://status.entergram.com)

## API Evangelist rating

**Kin Score 61.1** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 58.4 |
| Contract governance | 18.2 |
| Operational transparency | 50.0 |
| Developer ergonomics | 47.0 |
| Access clarity | 85.5 |

**Agent readiness 60.4** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | verified |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/entergram/](https://apis.io/providers/entergram/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Entergram: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/entergram/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
