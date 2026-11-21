# 0003. Rename API endpoint from /pet to /petapi in OpenAPI specification

* Status: proposed
* Date: 2026-11-21

## Context and Problem Statement

The OpenAPI (swagger.json) specification is being updated to change the endpoint path from /pet to /petapi. This alters the service contract for clients consuming the API.

## Decision Drivers

* Need to version or clarify the API endpoint naming
* Desire to avoid conflicts with previous or legacy endpoints
* Improve clarity or alignment with naming conventions

## Considered Options

### Rename /pet to /petapi
  * Good, because Avoids conflicts with existing endpoints
  * Good, because Clarifies the purpose or version of the endpoint
  * Bad, because Requires clients to update their integrations
  * Bad, because Potential for breaking changes if not communicated

### Keep /pet as is
  * Good, because No breaking changes for existing clients
  * Good, because No need for client updates
  * Bad, because Potential confusion with legacy endpoints
  * Bad, because Less clarity in endpoint naming

## Decision Outcome

The endpoint will be renamed from /pet to /petapi in the OpenAPI specification.

## Consequences

* Clients must update their integrations to use the new /petapi endpoint.
* Documentation and client SDKs may need to be regenerated or updated.
* Potential for temporary disruption if clients are not informed.

I APPROVE THIS
