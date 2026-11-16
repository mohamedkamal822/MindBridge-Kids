# Team structure and ownership

This project has seven members. The labels and issue owners below use the agreed member IDs; GitHub usernames have not been provided, so issues must not be assigned to accounts yet.

| Team | Members | Primary ownership |
|---|---|---|
| AI & NLP | M1 | LLM integration, Arabic conversation, intent recognition, RAG, knowledge base, prompts, response evaluation |
| Mobile app | M4, M5 | Flutter architecture, device matrix, navigation, API integration, scenario player, SQLite/offline work, camera/mic integration; Arabic RTL, child-friendly UI, AAC, caregiver/review-console UI, accessibility and usability protocol |
| Backend & database | M3 | FastAPI, PostgreSQL, authentication/authorization, consent, sessions, REST/scenario/content-pack APIs, progress/sync/deletion, role controls, OpenAPI and deployment |
| Data & intelligent inputs | M2, M6 | Sign dataset audit, MediaPipe landmarks, Random Forest baseline, evaluation and TFLite exploration; ASR/TTS/dialect evaluation, benchmark scenarios, synthetic examples, license register, content-review coordination |
| Project leader / QA & integration | M7 | Safety gate and red-team coordination, QA/test automation, CI/CD, ethics documentation, sprint management, integration, final report |

## Ownership and collaboration

- Module owners maintain their module README, setup instructions, tests, and decision notes.
- M3 publishes an OpenAPI contract early so M1 and M4/M5 can work independently against a stable interface.
- M7 coordinates cross-team acceptance, safety gate/red-team review, integration, ethics preparation, and release readiness; each feature still has a named implementer in its issue.
- M5 and M7 coordinate specialist/caregiver content review with M6. The app must not present itself as a diagnostic or therapeutic tool.
- Keep optional speech/sign work behind documented evaluation gates. It must not block the text-first MVP.
- Integrate changes through pull requests and test the interfaces where modules meet.
- Name a secondary member for each critical module to reduce single-person integration risk.

## Proposed module directories

Create `mobile/`, `backend/`, `ai/`, `intelligent-inputs/sign-recognition/`, `intelligent-inputs/speech-and-data/`, `safety/`, and `tests/` as implementation work is ready. Do not create empty app scaffolding just to satisfy the diagram. The proposed ownership is documented in each module README when that module is established.
