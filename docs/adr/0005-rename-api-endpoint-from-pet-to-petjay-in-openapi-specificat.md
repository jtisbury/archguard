# 0005. Rename API endpoint from /pet to /petjay in OpenAPI specification

* Status: proposed
* Date: 2026-11-23

## Context and Problem Statement

The API specification (swagger.json) has been updated to rename the endpoint from /pet to /petjay. This change affects the service contract exposed to API consumers.

## Decision Drivers

* Need to distinguish the endpoint for new functionality or versioning
* Avoid conflicts with existing /pet endpoint
* Clarify API usage for consumers

## Considered Options

### /petjay endpoint
  * Good, because Clear distinction from previous endpoints
  * Good, because Reduces ambiguity for consumers
  * Bad, because Requires client updates
  * Bad, because Potential for confusion if not documented

### Keep /pet endpoint
  * Good, because No client changes required
  * Good, because Maintains backward compatibility
  * Bad, because Does not address need for distinction or versioning

## Decision Outcome

The /pet endpoint is renamed to /petjay to provide a clear and distinct API contract for new or updated functionality.

## Consequences

* API consumers must update their integrations to use /petjay instead of /pet.
* Documentation and client SDKs need to be updated accordingly.
