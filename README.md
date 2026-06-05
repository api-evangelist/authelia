# Authelia (authelia)

Authelia is an open source authentication and authorization server providing multi-factor authentication and single sign-on for applications behind a reverse proxy. It supports OpenID Connect 1.0, OAuth 2.0, TOTP, WebAuthn, and Duo Push as authentication methods. Authelia exposes a REST API documented with an OpenAPI specification and integrates with nginx, Traefik, Caddy, and other reverse proxies.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/authelia/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/authelia/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Authentication
- Authorization
- LDAP
- MFA
- Open Source
- OpenID Connect
- Self-Hosted
- SSO

## Timestamps

- **Created:** 2026-03-25
- **Modified:** 2026-04-19

## APIs

### Authelia REST API

The Authelia REST API provides endpoints for authentication flows including first-factor login, MFA challenges, password reset, session management, and authorization verification for reverse proxy integration.

- **Human URL:** [https://www.authelia.com/reference/](https://www.authelia.com/reference/)
- **Base URL:** `https://your-authelia-instance.example.com/api`

#### Tags

- Authentication
- Authorization
- MFA
- REST
- SSO

#### Properties

- [Documentation](https://www.authelia.com/reference/)
- [OpenAPI](https://raw.githubusercontent.com/authelia/authelia/master/api/openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub Repository](https://github.com/authelia/authelia)
- [Postman Collection](collections/authelia.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authelia.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Authelia OpenID Connect 1.0 Provider

Authelia acts as an OpenID Certified OpenID Connect 1.0 Provider supporting Authorization Code, Implicit, and Hybrid flows with PKCE, PAR, and various token endpoint authentication methods.

- **Human URL:** [https://www.authelia.com/configuration/identity-providers/openid-connect/provider/](https://www.authelia.com/configuration/identity-providers/openid-connect/provider/)
- **Base URL:** `https://your-authelia-instance.example.com`

#### Tags

- Authentication
- OAuth
- OIDC
- OpenID Connect

#### Properties

- [Documentation](https://www.authelia.com/configuration/identity-providers/openid-connect/provider/)
- [Postman Collection](collections/authelia.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/authelia.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.authelia.com)
- [Documentation](https://www.authelia.com/configuration/prologue/introduction/)
- [GitHub Organization](https://github.com/authelia)
- [GitHub Repository](https://github.com/authelia/authelia)
- [Changelog](https://github.com/authelia/authelia/releases)
- [Support](https://github.com/authelia/authelia/discussions)
- [Community](https://discord.gg/authelia)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
