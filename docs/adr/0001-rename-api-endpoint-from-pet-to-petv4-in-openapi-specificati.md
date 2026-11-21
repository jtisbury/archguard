# 0001. Rename API endpoint from /pet to /petv4 in OpenAPI Specification

* Status: proposed
* Date: 2026-11-21

## Context and Problem Statement

The API specification (swagger.json) has been updated to change the endpoint path from /pet to /petv4. This alters the service contract for clients interacting with the API.

## Decision Drivers

* Need to version or differentiate the pet endpoint for new functionality or breaking changes
* Maintain backward compatibility or clarify API evolution
* Communicate changes clearly to API consumers

## Considered Options

### Rename /pet to /petv4
  * Good, because Allows introduction of breaking changes without affecting existing clients
  * Good, because Clarifies API versioning
  * Bad, because Requires clients to update their integrations
  * Bad, because May cause confusion if both endpoints are available

### Keep /pet and introduce changes in-place
  * Good, because No changes required for existing clients
  * Bad, because May break existing clients if changes are not backward compatible
  * Bad, because Harder to manage API evolution

## Decision Outcome

The /pet endpoint was renamed to /petv4 in the OpenAPI specification to introduce a new version of the endpoint, likely to support breaking changes or new features.

## Consequences

* Clients must update their integrations to use /petv4
* Documentation and client SDKs need to be regenerated or updated
* Potential for confusion if both endpoints are available simultaneously
