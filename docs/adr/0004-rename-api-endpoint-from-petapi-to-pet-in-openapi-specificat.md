# 0004. Rename API endpoint from /petapi to /pet in OpenAPI specification

* Status: proposed
* Date: 2026-11-23

## Context and Problem Statement

The OpenAPI specification (swagger.json) previously defined an endpoint at /petapi. This change renames the endpoint to /pet. Existing ADRs cover renaming from /pet to /petv4 and from /pet to /petapi, but not this reversal or new naming.

## Decision Drivers

* Align endpoint naming with business or domain conventions
* Consistency with other API endpoints
* Clarity for API consumers

## Considered Options

### Keep endpoint as /petapi
  * Good, because No changes required for existing clients
  * Bad, because May not align with naming conventions
  * Bad, because Potential confusion if /pet is the expected endpoint

### Rename endpoint to /pet
  * Good, because Aligns with expected or standard naming
  * Good, because Improves clarity for API consumers
  * Bad, because Requires clients to update their integrations

## Decision Outcome

The endpoint was renamed from /petapi to /pet to improve clarity and align with naming conventions.

## Consequences

* Clients using the old /petapi endpoint must update to use /pet.
* Documentation and client SDKs may need to be regenerated or updated.
