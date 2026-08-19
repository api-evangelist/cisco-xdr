---
name: cisco-xdr-respond-to-threat
description: Discover and execute a Cisco XDR response action against an observable — block, isolate or quarantine — through a configured integration module. High-consequence; requires an explicit human decision.
api: Cisco XDR Platform API (IROH)
generated: '2026-08-19'
method: generated
source: openapi/cisco-xdr-response-api-openapi.yml, openapi/cisco-xdr-moduleinstance-api-openapi.yml
operations:
  - GET /iroh/iroh-int/module-instance
  - POST /iroh/iroh-response/respond/observables
  - POST /iroh/iroh-response/respond/sighting
  - POST /iroh/iroh-response/respond/trigger/{module-instance-id}/{action-id}
scopes:
  - integration/module-instance:read
  - response/observables:read
  - response/sighting:read
  - response/trigger:write
consequence: irreversible-side-effect
---

# Take a response action in Cisco XDR

> **This skill changes the real world.** `respond/trigger` blocks domains, isolates endpoints and
> quarantines files through whatever product the module wraps. There is no test mode, no sandbox and
> no idempotency key. Do not call step 3 without an explicit, recorded human authorisation.

## Steps

1. **List what is configured** — `GET /iroh/iroh-int/module-instance`. You need a
   `module_instance_id` and its `module_type_id`; an action cannot be triggered without them.

2. **Discover available actions** — `POST /iroh/iroh-response/respond/observables` with the
   observable array. The response enumerates the actions each configured module offers for that
   observable, each with an `action_id`. Use `POST /iroh/iroh-response/respond/sighting` when you are
   acting on a sighting rather than a bare observable.

   Never guess an `action_id`. The provider documents this as a hard prerequisite: always call
   discovery first.

3. **Trigger** — `POST /iroh/iroh-response/respond/trigger/{module-instance-id}/{action-id}`, using
   the exact identifiers returned by step 2.

## Rules

- **Retry is not safe.** There is no `Idempotency-Key` on this operation. If the call times out you
  do not know whether the block landed. Re-run step 2 and inspect state before firing again —
  never blind-retry a trigger.
- **Scope separation is your safety rail.** `response/observables:read` and `response/sighting:read`
  let an agent discover actions; `response/trigger:write` is what lets it execute one. Issue API
  Clients with read-only response scopes for any agent that should investigate but not contain.
- **Confirm the module is healthy first.** A module instance can be `restricted` or degraded; the
  event catalogue carries `module-instance/restricted` and `module-instance/reactivated` events.
- Log the `trace_id` from any 5xx and hand it to `cisco-intel-api-support@cisco.com`.
- Rate limit is organization-wide (8000/hour); a runaway containment loop will lock out every other
  API client in the tenant.
