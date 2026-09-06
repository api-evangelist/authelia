---
name: authelia-oauth2-token-lifecycle
description: Obtain, introspect and revoke OAuth 2.0 tokens against an Authelia OpenID Connect 1.0 Provider, using its discovery documents rather than hardcoded paths.
api: authelia:authelia-oidc-api
generated: '2026-09-06'
method: generated
source: openapi/authelia-api-openapi.yml
operations:
  - getOpenIDConnectConfiguration
  - getOAuth2AuthorizationServerMetadata
  - getOpenIDConnectJSONWebKeySet
  - postOAuth2PushedAuthorizationRequest
  - postOpenIDConnectToken
  - postOAuth2Introspection
  - postOAuth2Revocation
  - getOpenIDConnectUserInfo
  - postOAuth2DeviceAuthorization
---

# OAuth 2.0 token lifecycle against Authelia

Authelia is an OpenID Certified™ Provider. Treat it as a standards-conformant authorization server: read
discovery first, and never hardcode endpoint paths.

## Steps

1. `getOpenIDConnectConfiguration` — `GET /.well-known/openid-configuration`. Every endpoint URL, supported
   grant type, response type, response mode, scope and client authentication method comes from here.
   `getOAuth2AuthorizationServerMetadata` (`GET /.well-known/oauth-authorization-server`, RFC 8414) is the
   OAuth 2.0-only equivalent.
2. `getOpenIDConnectJSONWebKeySet` — `GET /jwks.json` for the keys that verify issued tokens.
3. Obtain a token. Which path depends on the registered client:
   - Authorization Code with PKCE — the browser-mediated path. Optionally push the request first with
     `postOAuth2PushedAuthorizationRequest` (RFC 9126) and use the returned `request_uri`.
   - Device grant — `postOAuth2DeviceAuthorization` (RFC 8628), for input-constrained clients.
   - Client Credentials — `postOpenIDConnectToken` directly, for machine-to-machine.
4. `postOpenIDConnectToken` — `POST /api/oidc/token` exchanges the code or credentials. Authenticate the
   client with its registered `token_endpoint_auth_method`: `client_secret_basic`, `client_secret_post`,
   `client_secret_jwt`, `private_key_jwt`, or `none` for public clients.
5. `getOpenIDConnectUserInfo` — `GET /api/oidc/userinfo` with the access token. Because Authelia supports
   the claims parameter, the ID Token is deliberately minimal; scope-granted claims live here.
6. `postOAuth2Introspection` — `POST /api/oidc/introspection` (RFC 7662) to check a token is still active.
7. `postOAuth2Revocation` — `POST /api/oidc/revocation` (RFC 7009) to revoke. This is the reversal path for
   step 4.

## Rules

- Only tokens prefixed `authelia_at_` are access tokens. `authelia_rt_` is a refresh token and
  `authelia_ac_` is an authorization code; presenting either as a bearer token is rejected.
- The `authelia.bearer.authz` scope grants a token usable at the **proxy authorization** endpoints, not at
  the Authelia API. Authelia's own documentation is explicit about this. The token's audience must exactly
  match or prefix the URL being requested or authorization is denied.
- Errors use the RFC 6749 envelope: `{error, error_description, error_uri, error_hint, error_debug, state}`.
  Branch on `error`, which is a closed enumeration.
- Every OAuth 2.0 endpoint is rate limited by default at 30 requests/minute and 100/hour per deployment.
  Exhaustion returns 429 with **no** `Retry-After` header — back off for the bucket period.
- If the deployment enables the JWT Profile for Access Tokens, introspection becomes stateless and
  revocation is correspondingly weaker. Authelia discourages that profile for this reason.
