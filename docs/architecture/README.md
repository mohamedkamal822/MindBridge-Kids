# Architecture

This folder holds reviewed system diagrams, architecture decisions, data-flow descriptions, and integration boundaries. Record context, decision, alternatives, and consequences for each significant choice.

## Proposed component boundaries

- **Flutter client:** Android first, then iOS if feasible; child experience, parent-gated caregiver mode, SQLite content pack, generated Dart API client, OS secure storage for tokens. A minimal specialist review console may use Flutter Web and share models/client.
- **FastAPI backend:** authentication/authorization, consent, sessions, scenario/content-pack endpoints, progress events, deletion requests, and routing between deterministic and AI components. PostgreSQL stores only approved/minimal profile, content, and task data.
- **Deterministic activity engine:** selects reviewed scenarios, hints, allowed response shapes, and completion criteria. It owns permission checks, safety policy, supported sign vocabulary, and offline scripted fallbacks.
- **LLM/RAG:** interprets structured input and drafts constrained language using reviewed, licensed content. It does not choose permissions or activity sequence, diagnose, infer hidden emotional states, or improvise when offline. Safety checks bound input and output.
- **Optional input adapters:** Arabic speech transcription is shown for correction. Sign recognition runs on device where feasible and emits only supported text predictions/confidence; never upload video. Low confidence abstains and offers retry/AAC.

## Offline and data-flow requirements

Bundle a versioned, reviewed content pack containing scenarios, AAC metadata, and approved scripted responses. An unavailable network or AI service must not prevent the core text/card workflow; use the deterministic engine and reviewed scripts. Queue minimal task events locally with idempotent event IDs and sync them later. Keep names, raw media, and child free-text outside durable local storage beyond the active session; define retention/deletion for every persisted event. Store tokens in OS secure storage.

## Child safety and access boundaries

The child mode stays free of ads, purchases, external links, child push notifications, and behavioral analytics SDKs. Request camera/microphone permissions only when the corresponding mode opens, explain them plainly, and keep the app usable without them. A parent gate protects caregiver/settings areas, consent, and deletion. Use role-based access and audit caregiver/specialist views. Caregiver summaries show tasks and skills practiced, not inferred emotion or hidden scores. Specialist-approved adult-support wording must be reachable from every child screen.

This is a planning architecture, not evidence of implementation. Obtain specialist input and applicable institutional ethics/privacy review before research or a child-facing pilot. Keep speech/sign optional so they cannot delay the text-first MVP.
