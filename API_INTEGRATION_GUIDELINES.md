# API integration guidelines

## Contract first

M3 owns the FastAPI contract and should publish an initial OpenAPI document by month two (with a draft resource map in month one). Commit the reviewed contract under `docs/api/` and expose the generated FastAPI OpenAPI document during backend development. Mobile and AI teams should be able to build against examples and schemas without waiting for backend implementation. Generate the Dart client from the accepted schema rather than hand-maintaining divergent request models.

## Contract contents

Document for every endpoint: purpose, method/path, request and response schemas, validation limits, authentication requirements, error codes, privacy classification, and at least one safe example. Define versioning and deprecation rules before clients depend on the API. Never put real child data or credentials in examples.

## Integration agreements

- Use Pydantic models as the backend source of truth; review schema changes with M1 and M4/M5.
- Agree on stable IDs, timestamps/time zones, Arabic text encoding, pagination, and error response format.
- Keep authentication/session behavior explicit; send credentials only over TLS and never log them.
- Define what is stored locally in SQLite versus remotely in PostgreSQL, versioned/checksummed content-pack refresh, offline conflict behavior, idempotent task-event sync, and deletion semantics before implementation.
- Specify caregiver consent/revocation and role scopes. Caregiver/specialist progress endpoints return permitted task/skill summaries, not inferred emotional state or hidden scores; audit those views.
- Keep optional sign input on-device. If a future endpoint is justified, it accepts landmarks only and never video.
- Include an authorized deletion-request flow and define which minimal records remain, if any, to satisfy an approved retention policy.
- Raw child audio/video is not stored by default. Any optional media endpoint requires an approved data-flow and retention design.
- Use mock responses or a generated client from the contract for parallel development; keep contract validation in deterministic CI.

## Contract change checklist

1. Update the OpenAPI contract and safe examples.
2. Add/update Pydantic schema and endpoint tests.
3. Notify mobile and AI owners and identify compatibility impact.
4. Update client mappings and integration tests.
5. Merge through reviewed pull requests to `develop`.
