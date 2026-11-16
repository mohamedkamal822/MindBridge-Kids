# Backend (planned)

**Owner:** M3.

The planned FastAPI service owns authentication/authorization, consent, sessions, REST/scenario/content-pack APIs, minimal progress events, PostgreSQL persistence, sync/deletion behavior, and the OpenAPI contract. Publish a draft resource map in Month 1 and OpenAPI v1 by Month 2 so mobile and AI teams can work in parallel. The specialist review console needs authenticated, role-limited review endpoints.

The API is a gateway and boundary enforcer; it should route requests through structured input adapters, context management, a deterministic activity engine, constrained LLM/RAG, and an independent safety gate. The activity engine—not an LLM agent—owns sequence, permissions, completion criteria, supported vocabulary, and offline scripted fallback. Record only necessary pseudonymous task events; use idempotent event IDs for sync. Caregiver/specialist reads need role checks and audit events. Raw child audio/video is not stored by default; optional sign recognition sends landmarks only if a separately reviewed need exists.

No backend application is scaffolded yet. Add implementation and dependency manifests with the first real vertical slice; document local services, migrations, auth/consent, API run commands, data retention/deletion, and tests here. Endpoint ideas in [docs/api/README.md](../docs/api/README.md) are illustrative, not an accepted contract.
