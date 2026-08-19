---
name: cisco-xdr-investigate-observable
description: Investigate an observable (IP, domain, file hash, URL, email) across every configured Cisco XDR integration — extract it from text, get sightings and verdicts, and collect pivot links — then record the finding in a casebook.
api: Cisco XDR Platform API (IROH)
generated: '2026-08-19'
method: generated
source: openapi/cisco-xdr-inspect-api-openapi.yml, openapi/cisco-xdr-observe-api-openapi.yml, openapi/cisco-xdr-deliberate-api-openapi.yml, openapi/cisco-xdr-refer-api-openapi.yml, openapi/cisco-xdr-casebook-api-openapi.yml
operations:
  - POST /iroh/iroh-inspect/inspect  # findObservables — the only operationId in the IROH/CTIA surface
  - POST /iroh/iroh-enrich/observe/observables
  - POST /iroh/iroh-enrich/deliberate/observables
  - POST /iroh/iroh-enrich/refer/observables
  - POST /ctia/casebook
  - POST /ctia/casebook/{id}/observables
scopes:
  - inspect:read
  - enrich/observables/observe:read
  - enrich/observables/deliberate:read
  - enrich/observables/refer:read
  - casebook
---

# Investigate an observable in Cisco XDR

## Before you start

Get a token. Cisco XDR uses OAuth 2.0 client credentials, and the token is short-lived — 600 seconds
in the documented example, so refresh rather than cache across a long run.

```
POST https://visibility.amp.cisco.com/iroh/oauth2/token
Authorization: Basic base64(client_id:client_password)
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials
```

Use `Authorization: Bearer <access_token>` on every subsequent call. Swap `visibility.amp.cisco.com`
for `visibility.eu.amp.cisco.com` or `visibility.apjc.amp.cisco.com` outside North America.

## Steps

1. **Extract observables from free text** — `POST /iroh/iroh-inspect/inspect` with `{"content": "<text>"}`.
   This is the one operation in the whole IROH/CTIA surface that declares an operationId
   (`findObservables`). It returns typed observables; you do not have to parse IOCs yourself.

2. **Observe** — `POST /iroh/iroh-enrich/observe/observables` with the observable array as the body.
   Note the body is the array itself, not `{"observables": [...]}` — the provider's own MCP notes
   record this as a source of 400s. This returns sightings from every configured module.

3. **Deliberate** — `POST /iroh/iroh-enrich/deliberate/observables` for verdicts and dispositions.
   Faster than observe; use it when you only need "is this bad".

4. **Refer** — `POST /iroh/iroh-enrich/refer/observables` for pivot links into each product console.

5. **Record it** — `POST /ctia/casebook` on `https://private.intel.amp.cisco.com` to open a casebook,
   then `POST /ctia/casebook/{id}/observables` to attach what you found.

## Rules

- **Read the errors on a 200.** Enrich responses aggregate across modules. A 200 can carry an
  `ErrorMessage` per module (`module_instance_id`, `code`, `message`, `type: fatal|warning|error`)
  while other modules succeeded. Treat a 200 with fatal module errors as a partial result, not a
  success.
- **Three error envelopes, no RFC 9457.** IROH returns `{error, error_description, error_code,
  error_uri, trace_id}`. Conure returns `{message}`. Quote the `trace_id` from a 500 when you escalate.
- **No idempotency key exists.** Retrying `POST /ctia/casebook` creates a second casebook. Set an
  `external_id` on create and check `GET /ctia/casebook/external_id/{external_id}` before retrying.
- **Rate limit is per organization, not per client**: 8000 requests/hour on a rolling window. On 429,
  read `Retry-After` and `X-Ratelimit-Org-Remaining`.
- Hosts differ per family. Inspect and Enrich live on `visibility.amp.cisco.com/iroh`; casebooks and
  all threat-intel entities live on `private.intel.amp.cisco.com/ctia`. Mixing them returns 404.
