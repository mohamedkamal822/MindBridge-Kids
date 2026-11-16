# Data, content, and evaluation plan

This is a planning register, not confirmation that data is available, licensed for this use, or approved. M6 maintains the source/license inventory and coordinates content review; M2 leads sign-data evaluation; M1 owns AI/RAG evaluation. Verify the authoritative source page, current version, license, consent/provenance, access conditions, attribution, modification, and redistribution terms before access or use. Ask the supervisor/institution about ethics requirements before collecting data or involving children.

## Candidate sources to audit

| Candidate named in the planning document | Potential use | Audit before use |
|---|---|---|
| Egyptian Sign Language dataset, Mendeley record `39tbt2jd7r/3` | Limited-vocabulary baseline | Verify current record/version, exact license/attribution, consent/provenance, labels, signer count, recording conditions and permitted redistribution; test signer-independent splits. The planning document reports CC BY 4.0 and 55 classes/400+ clips; these are unverified claims, not project findings. |
| Mozilla Common Voice Arabic | ASR component baseline | Verify release-specific access/license and dialect/speaker metadata. Read speech may not represent children or Egyptian conversational Arabic. The planning document reports CC0-1.0; verify the exact release terms. |
| ARASAAC | AAC symbol candidates | Verify current terms, attribution, share-alike/noncommercial implications, and cultural/semantic suitability with reviewers before bundling. |
| CHILDES/TalkBank | Research reference only where appropriate | Access and reuse rules vary; review source-specific terms. Do not treat it as a ready-made Arabic emotional-awareness dataset. |
| Project-authored synthetic benchmark | Scenario, response, and safety evaluation | Record authorship/permissions, reviewer and version; synthetic results do not establish real-world effectiveness. |

Record source URL, access date, version, license evidence, consent/provenance, intended use, transformations, restrictions, attribution, reviewer, storage location, and decision. Keep restricted datasets and sensitive annotations out of Git. Do not upload private samples to issues or PRs.

## Proposed benchmark plan

Planning targets from the project specification are **100–200 structured scenarios** and **300–500 synthetic example dialogues**; they are not current dataset counts or mandatory success criteria. Candidate skills include asking for help, expressing a preference, requesting a break, starting a conversation, expressing confusion, taking turns, and respecting boundaries.

Each item should record age band, target skill, scenario/source, acceptable response patterns, review status, version, and license/allowed use. Include ambiguous inputs that should trigger clarification and specialist-reviewed safety cases. Split development/validation/test data and keep test items out of prompt tuning.

## Evaluation evidence

- **Speech:** WER or task-specific transcription accuracy by dialect/noise condition; show and allow correction of transcripts.
- **Sign:** signer-independent test split, per-class precision/recall, macro-F1, confusion matrix, abstention, on-device latency/battery, and desktop-to-TFLite performance change.
- **RAG/LLM:** retrieval relevance, source correctness/grounding, unsupported-claim rate, age appropriateness, skill alignment, clarity, safety, and specialist rubric agreement.
- **Mobile/system:** offline success, crash-free sessions, startup/screen latency, service-failure recovery, accessibility checks, and device-matrix coverage; establish thresholds after baseline measurement.
- **Usability:** task completion against a predefined rubric, meaning preservation, retries/help requests, alternative-modality availability, and caregiver/specialist feedback.

Begin with synthetic/offline testing and specialist review. Any evaluation with children requires applicable ethics approval, guardian consent, child assent, safe facilitation, and an appropriate study plan. Do not claim clinical or mental-health benefit from engagement or task completion.
