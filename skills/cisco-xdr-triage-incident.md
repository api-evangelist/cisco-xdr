---
name: cisco-xdr-triage-incident
description: Triage Cisco XDR incidents — search high-priority incidents, pull an incident's observables, events and worklog, update its status and assignee, and append a worklog note.
api: Cisco XDR Incidents & Investigations API (Conure v2) + CTIA
generated: '2026-08-19'
method: generated
source: openapi/cisco-xdr-incidents-investigations-openapi.json, openapi/cisco-xdr-incident-api-openapi.yml, openapi/cisco-xdr-event-api-openapi.yml
operations:
  - GET /v2/incident/search
  - GET /v2/incident/search/count
  - GET /v2/incident/{incident-id}
  - GET /v1/incident/{incident-id}/assets
  - GET /ctia/incident/{id}
  - PATCH /ctia/incident/{id}
  - POST /ctia/incident/{id}/status
  - POST /ctia/note
  - GET /iroh/iroh-event/event/incident/{incident-id}
scopes:
  - private-intel/incident:read
  - private-intel/incident:write
  - private-intel/note:write
  - event:read
---

# Triage a Cisco XDR incident

## Which host

Incident **search** is Conure v2 on `https://conure.us.security.cisco.com`. Incident **read and
write** is CTIA on `https://private.intel.amp.cisco.com`. Cisco's own MCP server changed from the
IROH incident path to Conure v2 in its v2.1.0 release precisely because the IROH path 404d — do not
assume one host serves both.

## Steps

1. **Find the incidents** — `GET /v2/incident/search` with `status`, `from`, `to`, `limit`, `offset`.
   Default to a bounded window; the provider's own client defaults to the last 30 days.
   `GET /v2/incident/search/count` gives the total without paging.

2. **Read it** — `GET /v2/incident/{incident-id}` for the search-shaped document, or
   `GET /ctia/incident/{id}` for the full CTIM entity. They are not the same shape.

3. **Widen the picture** —
   `GET /v1/incident/{incident-id}/assets` for affected assets, and
   `GET /iroh/iroh-event/event/incident/{incident-id}` for the combined Private Intel + IROH event
   timeline. Events are signed and carry an emitter, so you can attribute each change.

4. **Update** — `PATCH /ctia/incident/{id}` for status, assignee and resolution, or
   `POST /ctia/incident/{id}/status` for a status-only transition. PATCH can return 204 No Content;
   do not treat an empty body as a failure.

5. **Leave a trail** — `POST /ctia/note` to append a worklog entry. Say what you changed and why.

## Rules

- **Never take a response action from this skill.** Containment lives in
  `cisco-xdr-respond-to-threat` and is deliberately separate.
- **No idempotency.** A retried `POST /ctia/note` writes a duplicate worklog entry. Use `external_id`
  and check `GET /ctia/note/external_id/{external_id}` first.
- Paginate CTIA searches with `search_after` and the `X-Sort` response header, not deep `offset` —
  `search_after` is the cursor Cisco actually intends (it appears on 157 operations).
- 406 is real: CTIA and Conure negotiate JSON, YAML, EDN and Transit. Send `Accept: application/json`.
