# Authelia (authelia)
Authelia is an open source authentication and authorization server providing multi-factor authentication and single sign-on for applications behind a reverse proxy. It supports OpenID Connect 1.0, OAuth 2.0, TOTP, WebAuthn, and Duo Push as authentication methods. Authelia exposes a REST API documented with an OpenAPI specification and integrates with nginx, Traefik, Caddy, and other reverse proxies.

**URL:** [https://www.authelia.com](https://www.authelia.com)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Authentication, Authorization, LDAP, MFA, Open Source, OpenID Connect, Self-Hosted, SSO

## Timestamps

- **Created:** 2026-03-25
- **Modified:** 2026-04-19

## APIs

### Authelia REST API
The Authelia REST API provides endpoints for authentication flows including first-factor login, MFA challenges, password reset, session management, and authorization verification for reverse proxy integration.

**Human URL:** [https://www.authelia.com/reference/](https://www.authelia.com/reference/)

#### Tags:

 - Authentication, Authorization, MFA, REST, SSO

#### Properties

- [Documentation](https://www.authelia.com/reference/)
- [OpenAPI](https://raw.githubusercontent.com/authelia/authelia/master/api/openapi.yml)
- [GitHubRepository](https://github.com/authelia/authelia)

### Authelia OpenID Connect 1.0 Provider
Authelia acts as an OpenID Certified OpenID Connect 1.0 Provider supporting Authorization Code, Implicit, and Hybrid flows with PKCE, PAR, and various token endpoint authentication methods.

**Human URL:** [https://www.authelia.com/configuration/identity-providers/openid-connect/provider/](https://www.authelia.com/configuration/identity-providers/openid-connect/provider/)

#### Tags:

 - Authentication, OAuth, OIDC, OpenID Connect

#### Properties

- [Documentation](https://www.authelia.com/configuration/identity-providers/openid-connect/provider/)

## Common Properties

- [Website](https://www.authelia.com)
- [Documentation](https://www.authelia.com/configuration/prologue/introduction/)
- [GitHubOrganization](https://github.com/authelia)
- [GitHubRepository](https://github.com/authelia/authelia)
- [ChangeLog](https://github.com/authelia/authelia/releases)
- [Support](https://github.com/authelia/authelia/discussions)
- [Community](https://discord.gg/authelia)

## Features

| Name | Description |
|------|-------------|
| Multi-Factor Authentication | Supports TOTP, WebAuthn/FIDO2, Duo Push, and mobile authenticator apps as second factors. |
| OpenID Connect 1.0 Provider | OpenID Certified identity provider supporting Authorization Code, Implicit, and Hybrid flows. |
| Single Sign-On | Session-based SSO across all applications behind the reverse proxy with configurable session lifetime. |
| LDAP/Active Directory Integration | User authentication against LDAP, Active Directory, and OpenLDAP directories with group-based access control. |
| Access Control Rules | Fine-grained access control policies based on domain, path, user, group, and network for precise authorization. |
| Reverse Proxy Integration | Native integration with nginx, Traefik, Caddy, HAProxy, Envoy, and Skipper via forward-auth and ExtAuthz endpoints. |
| Passwordless Authentication | Support for WebAuthn/FIDO2 passwordless login using hardware security keys and platform authenticators. |

## Use Cases

| Name | Description |
|------|-------------|
| Self-Hosted SSO | Deploy a self-hosted SSO solution for internal web applications and services without relying on cloud identity providers. |
| Homelab Security | Protect self-hosted homelab applications with MFA and access control without exposing them to the internet unprotected. |
| Small Business Identity | Provide centralized authentication for small business web applications using LDAP and access control policies. |
| OIDC Provider | Act as an OpenID Connect provider for applications requiring OAuth 2.0 and OIDC-based authentication flows. |

## Integrations

| Name | Description |
|------|-------------|
| Nginx | Integration with nginx-based proxies including nginx, nginx-proxy-manager, and Swag via auth_request module. |
| Traefik | Native Traefik middleware integration via ForwardAuth for seamless authentication in Docker and Kubernetes environments. |
| Caddy | Caddy forward-auth integration for protecting applications behind the Caddy web server. |
| LDAP/Active Directory | User directory integration with LDAP, Active Directory, and FreeIPA for enterprise user management. |
| Helm | Official Helm chart available at the authelia/chartrepo GitHub repository for Kubernetes deployment. |

## Solutions

| Name | Description |
|------|-------------|
| Self-Hosted Identity | Complete self-hosted identity and access management solution for privacy-conscious deployments. |
| Zero Trust Security | Enforce zero trust network access policies for internal applications with per-request authentication verification. |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
