# 0006. Change API basePath from /v2 to /v3 and rename /user endpoint to /createuser in OpenAPI specification

* Status: proposed
* Date: 2026-11-23

## Context and Problem Statement

The OpenAPI (swagger.json) specification has been updated to change the API basePath from /v2 to /v3 and to rename the /user endpoint to /createuser. This impacts how clients interact with the API and may affect routing, versioning, and client integrations.

## Decision Drivers

* Need to version the API to reflect breaking changes or new features
* Desire to clarify or better represent the purpose of the /user endpoint by renaming it to /createuser
* Maintain consistency and clarity in API endpoints for consumers

## Considered Options

### Change basePath to /v3 and rename /user to /createuser
  * Good, because Clearly communicates a new API version
  * Good, because Endpoint naming is more descriptive
  * Bad, because Requires clients to update their integrations
  * Bad, because Potential for breaking changes if not communicated properly

### Keep basePath as /v2 and endpoint as /user
  * Good, because No breaking changes for existing clients
  * Good, because No need for immediate client updates
  * Bad, because Does not reflect new version or changes in API
  * Bad, because Endpoint name may be less descriptive

## Decision Outcome

The basePath will be updated to /v3 and the /user endpoint will be renamed to /createuser in the OpenAPI specification.

## Consequences

* Clients must update their integrations to use the new basePath and endpoint name
* Documentation and client SDKs may need to be regenerated or updated
* Potential for confusion if changes are not communicated effectively
