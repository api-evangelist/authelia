---
name: authelia-manage-second-factor-credentials
description: Enumerate and remove a user's own TOTP and WebAuthn credentials on an Authelia deployment, including the session elevation the flow requires.
api: authelia:authelia-api
generated: '2026-09-06'
method: generated
source: openapi/authelia-api-openapi.yml
operations:
  - getState
  - getUserInfo
  - getUserSessionElevation
  - postUserSessionElevation
  - putUserSessionElevation
  - deleteUserSessionElevation
  - getSecondFactorWebAuthnCredentials
  - deleteSecondFactorWebAuthnCredential
  - getSecondFactorTOTPConfiguration
  - deleteSecondFactorTOTP
  - postUserInfoSecondFactorMethod
---

# Manage your own second factor credentials

Credential management is the most destructive surface on the Authelia API and it is gated twice: by
authentication level and by an elevated session.

## Steps

1. `getState` — confirm the authentication level is 2FA. A 1FA session cannot manage credentials.
2. `getUserInfo` — `GET /api/user/info` returns the user's registered methods and preferred method.
3. `getUserSessionElevation` — `GET /api/user/session/elevation`. If the session is not already elevated:
   - `postUserSessionElevation` starts the flow; Authelia sends a one-time code to the user's registered
     address. **This requires a human.** An agent cannot complete it alone.
   - `putUserSessionElevation` finishes the flow with the code.
   - The elevation expires on its own; `deleteUserSessionElevation` revokes it early and is the correct
     cleanup step once the work is done.
4. `getSecondFactorWebAuthnCredentials` — `GET /api/secondfactor/webauthn/credentials` lists the user's
   registered credentials. Each has a `credentialID` used as the path parameter.
5. `deleteSecondFactorWebAuthnCredential` — `DELETE /api/secondfactor/webauthn/credential/{credentialID}`.
6. `getSecondFactorTOTPConfiguration` / `deleteSecondFactorTOTP` — read and remove the TOTP configuration.
7. `postUserInfoSecondFactorMethod` — set the preferred second factor method after the change.

## Rules

- **Deletion is irreversible.** There is no restore, no undo window and no trash. A removed WebAuthn
  credential requires the physical authenticator to re-register; a removed TOTP configuration destroys the
  shared secret. Confirm with the user before either delete.
- Removing the user's last second factor can lock them out if the deployment's access control policy
  requires 2FA. Check `getUserInfo` for remaining methods first.
- There is **no idempotency key** on this API. A retried DELETE is not automatically safe — re-read the
  credential list rather than blindly repeating the call.
- Session elevation start and finish are rate limited by default: 3 requests per 5 minutes (start) and
  3 per 10 minutes (finish). A 429 means back off for the bucket period; no Retry-After header is sent.
