---
name: authelia-verify-deployment-state
description: Read an Authelia deployment's configuration, health and the caller's current session state before attempting any authenticated operation.
api: authelia:authelia-api
generated: '2026-09-06'
method: generated
source: openapi/authelia-api-openapi.yml
operations:
  - getHealth
  - getConfiguration
  - getPasswordPolicyConfiguration
  - getState
---

# Verify an Authelia deployment's state

Authelia is self-hosted. There is no vendor host and no API key — the base URL is whatever host the
operator deployed, and every authenticated call is scoped to the caller's own session cookie. Establish
those facts before anything else.

## Steps

1. `getHealth` — `GET /api/health` on the deployment base URL. A 200 means the server is up. `headHealth`
   is the same check without a body.
2. `getConfiguration` — `GET /api/configuration`. Returns which second factor methods this deployment has
   enabled and the TOTP period. Never assume TOTP, WebAuthn or Duo are available; this endpoint is the only
   authority for a given deployment.
3. `getPasswordPolicyConfiguration` — `GET /api/configuration/password-policy`. Read this before proposing
   any password value in a change or reset flow.
4. `getState` — `GET /api/state`. Returns the caller's authentication level. Branch on it:
   - anonymous — nothing else on the portal API will succeed.
   - 1FA — password verified; credential management will be refused.
   - 2FA — second factor completed.

## Rules

- HTTPS is mandatory. Authelia refuses to be served over plain HTTP by design.
- Auth is the `authelia_session` cookie (name is a per-deployment default, configurable). There is no API
  key, bearer token or personal access token for this API.
- Errors come back as `{"status":"KO","message":"..."}` with no machine-readable code. Branch on the HTTP
  status, not on the message.
- A 403 here usually means the authentication level is too low, not that the operation does not exist.
