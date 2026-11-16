# API documentation

Store the reviewed, versioned OpenAPI contract and API usage examples here. M3 owns the backend contract and should publish it by Month 2 (draft resource map in Month 1), early enough for mobile and AI teams to work independently. The endpoint list below is illustrative from the planning specification; it is not an implemented contract.

## Proposed resource map

- `POST /auth/login`, `POST /auth/refresh`: caregiver/specialist authentication and short-lived access tokens.
- `POST /consent`: record or revoke consent for a defined purpose.
- `POST /sessions`, `POST /sessions/{id}/message`: create a goal-bound session and submit text or confirmed transcription with structured intent/confidence/modality fields.
- `GET /scenarios`, `GET /content/packs/latest`: list approved scenarios and fetch a versioned/checksummed offline pack.
- `POST /sessions/{id}/activity-result`: submit a minimal, idempotent task event.
- `GET /care/progress/{pseudonymous_id}`: role-authorized task/skill summary only.
- `POST /review/feedback`: authorized specialist rubric feedback.
- `DELETE /users/{id}/data`: process a caregiver deletion request under documented retention rules.
- Optional sign fallback accepts landmark vectors only; never video. Keep this out of MVP contract unless the sign module passes its go/no-go review.

The API should include validation/errors, roles/scopes, privacy classification, deletion/sync semantics, and safe synthetic examples. Generate the Dart client from the accepted OpenAPI schema. See [API_INTEGRATION_GUIDELINES.md](../../API_INTEGRATION_GUIDELINES.md).
