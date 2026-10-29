# Authelia

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

Authelia is an open source authentication and authorization server providing multi-factor authentication and single sign-on for applications behind a reverse proxy. It supports OpenID Connect 1.0, OAuth 2.0, TOTP, WebAuthn, and Duo Push as authentication methods. Authelia exposes a REST API documented with an OpenAPI specification and integrates with nginx, Traefik, Caddy, and other reverse proxies.

**Areas:** Authentication · Authorization · LDAP · MFA · Open Source · OpenID Connect · Self-Hosted · SSO · Identity Federation

## Authelia on APIs.io

Everything profiled for Authelia is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/authelia/](https://apis.io/providers/authelia/)** — or go straight to one of the APIs or properties below.

### APIs (13)

- [Authelia OpenID Connect 1.0 Provider](https://apis.io/apis/authelia/authelia-oidc-provider/) — Authelia acts as an OpenID Certified OpenID Connect 1.0 Provider supporting Authorization Code, Implicit, and Hybrid flows with PKCE, PAR, and various token…
- [Authelia Authentication API](https://apis.io/apis/authelia/authelia-authentication-api/) — Authentication endpoints
- [Authelia Authorization API](https://apis.io/apis/authelia/authelia-authorization-api/) — Authorization endpoints
- [Authelia First Factor API](https://apis.io/apis/authelia/authelia-first-factor-api/) — First Factor Authentication
- [Authelia OAuth 2.0 API](https://apis.io/apis/authelia/authelia-oauth-2-0-api/) — OAuth 2.0 Endpoints
- [Authelia OpenID Connect 1.0 API](https://apis.io/apis/authelia/authelia-openid-connect-1-0-api/) — OpenID Connect 1.0 Endpoints
- [Authelia Password Change API](https://apis.io/apis/authelia/authelia-password-change-api/) — Password change endpoint
- [Authelia Password Reset API](https://apis.io/apis/authelia/authelia-password-reset-api/) — Password reset endpoints
- [Authelia Second Factor API](https://apis.io/apis/authelia/authelia-second-factor-api/) — TOTP, WebAuthn and Duo endpoints
- [Authelia State API](https://apis.io/apis/authelia/authelia-state-api/) — Configuration, health and state endpoints
- [Authelia User Elevation API](https://apis.io/apis/authelia/authelia-user-elevation-api/) — User session elevation endpoints
- [Authelia User Information API](https://apis.io/apis/authelia/authelia-user-information-api/) — User configuration endpoints
- [Authelia Utilities API](https://apis.io/apis/authelia/authelia-utilities-api/) — General utilities used in several operations

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [authelia-mcp.yml](https://apis.io/servers/authelia/authelia-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Authelia Agentic Access](https://apis.io/agentic-access/authelia/authelia-agentic-access/)

#### JSON Schema (5)

The data models the API reads and writes.

- [Authelia Configuration.Schema](https://apis.io/schemas/authelia/authelia-configuration.schema/)
- [Authelia Exports.Identifiers.Schema](https://apis.io/schemas/authelia/authelia-exports.identifiers.schema/)
- [Authelia Exports.Totp.Schema](https://apis.io/schemas/authelia/authelia-exports.totp.schema/)
- [Authelia Exports.Webauthn.Schema](https://apis.io/schemas/authelia/authelia-exports.webauthn.schema/)
- [Authelia User Database.Schema](https://apis.io/schemas/authelia/authelia-user-database.schema/)

#### Collections (3)

Postman and Open Collection request collections.

- [Authelia OpenID Connect 1.0 Endpoints](https://apis.io/collections/authelia/open-authelia/)
- [Authelia OpenID Connect 1.0 Endpoints Discovery API](https://apis.io/collections/authelia/open-authelia-discovery-api/)
- [Authelia OpenID Connect 1.0 Endpoints Discovery OIDC API](https://apis.io/collections/authelia/open-authelia-oidc-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Authelia Api Overlay](https://apis.io/overlays/authelia/authelia-api-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Authelia Authentication](https://apis.io/security/authelia/authelia-authentication/)
- [Authelia Domain Security](https://apis.io/security/authelia/authelia-domain-security/)
- [Authelia Vulnerability Disclosure](https://apis.io/security/authelia/authelia-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Authelia Scopes](https://apis.io/scopes/authelia/authelia-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Authelia Plans Pricing](https://apis.io/plans/authelia/authelia-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Authelia Rate Limits](https://apis.io/rate-limits/authelia/authelia-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Authelia Finops](https://apis.io/finops/authelia/authelia-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.authelia.com)
- [Documentation](https://www.authelia.com/configuration/prologue/introduction/)
- [Getting started](https://www.authelia.com/integration/prologue/get-started/)
- [API reference](https://www.authelia.com/reference/)
- [Support](https://github.com/authelia/authelia/discussions)
- [Changelog](https://github.com/authelia/authelia/releases)
- [Blog](https://www.authelia.com/blog/)
- [Privacy policy](https://www.authelia.com/policies/privacy/)
- [GitHub](https://github.com/authelia)

## API Evangelist rating

**Kin Score 53.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 50.8 |
| Contract governance | 18.2 |
| Operational transparency | 73.7 |
| Developer ergonomics | 56.5 |
| Access clarity | 10.5 |

**Agent readiness 31.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | verified |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 36.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/authelia/](https://apis.io/providers/authelia/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Authelia: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/authelia/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
