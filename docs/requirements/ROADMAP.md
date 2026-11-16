# Eight-month roadmap

| Month | Milestone | Exit evidence |
|---|---|---|
| 1 | Repository/CI and environment setup; requirements, architecture and ethics planning; device survey; dataset/license audit; scenario taxonomy | Reviewed requirements and risk/ethics plan, architecture decisions, device/OS survey, verified-source register, agreed scenario taxonomy |
| 2 | Arabic RTL design system and clickable prototype; OpenAPI v1; database and scenario schemas; MVP/architecture freeze | Reviewed prototype, versioned API/schema, first curated content, signed-off MVP scope and Flutter architecture |
| 3 | Text-first Android MVP on a real device | Guided chat/scenario player, intent schema, auth/session/API path, offline store and first benchmark items demonstrated on device |
| 4 | Social scenarios, AAC, progress events, safety gate, offline content-pack pipeline | Reviewed scenario/AAC flow, deterministic safety checks, approved offline content and sync behavior |
| 5 | Speech/sign benchmarks and optional-module go/no-go; camera/mic integration only against evaluated needs | Reproducible benchmark reports and explicit continue/simplify/drop decision; optional work cannot delay core MVP |
| 6 | Parent gate, permissions, caregiver dashboard, specialist review console; end-to-end integration and feature freeze | Reviewed caregiver/specialist flows, integrated beta, red-team results and frozen feature scope |
| 7 | Technical/device-matrix testing, specialist review and approved usability evaluation | Reproducible evaluation report with limitations, error analysis, accessibility and safety findings |
| 8 | Bug fixing, reproducibility package, final documentation/report and demonstration | Release candidate, final report/demo and known limitations documented |

## First-month plan

1. M7 sets up repository workflow, labels, CI, ethics/safety planning and team cadence; the board and branch settings are completed by an admin.
2. M3 drafts the FastAPI resource map, auth/consent/session needs and OpenAPI sketch; M1 reviews structured intent, RAG and safety boundaries.
3. M2 audits Egyptian Sign Language dataset availability, licensing, consent/provenance, signer coverage and feasibility before use.
4. M6 creates the source/license register, coordinates specialist content review, and drafts synthetic scenario/safety benchmark criteria.
5. M4 surveys test devices/minimum OS constraints and proposes the Flutter architecture; M5 drafts the Arabic RTL design system and clickable child-flow prototype.
6. All members review non-goals, data flows, research/ethics prerequisites, MVP acceptance criteria, and the scenario taxonomy.

Checkpoint gates: freeze MVP/API/Flutter architecture at the end of Month 2; require a real-device text-first MVP by end of Month 3 or cut optional work; decide speech/sign go/no-go by end of Month 5; feature freeze at end of Month 6.

The task-level starter backlog is in [STARTER_BACKLOG.md](STARTER_BACKLOG.md).
