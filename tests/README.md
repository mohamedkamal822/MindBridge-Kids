# Tests and evaluation

**Coordinator:** M7; each module owner maintains its unit and contract tests.

Keep tests deterministic and self-contained. CI must not call live LLM/ASR/TTS services or require secrets. Use synthetic fixtures. As modules land, cover:

- Pydantic/OpenAPI request and response schemas, role/consent boundaries, and idempotent offline event sync.
- Text/AAC and bundled-scenario behavior when network, LLM, speech, or sign services are unavailable.
- Deterministic intent/response constraints, RAG source/grounding behavior using fixtures, uncertainty/clarification, and independent safety-gate cases.
- Privacy invariants: no raw media persistence/upload by default, no child data in logs, caregiver/specialist access auditing, and deletion behavior.
- Flutter RTL/accessibility behavior, 48 dp target audit, screen-reader/text scaling, parent gate, permission-denied flows, and device/offline integration checks.
- Research evaluations with separate train/validation/test partitions and documented metrics; do not represent synthetic evaluation as evidence of clinical effectiveness.

Organize cross-module integration and safety checks here as implementation develops, and document limitations in evaluation reports. Real-device/device-matrix and specialist review are release activities and cannot be replaced by unit tests.
