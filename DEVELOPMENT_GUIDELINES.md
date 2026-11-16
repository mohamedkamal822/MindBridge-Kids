# Development guidelines

## Product and safety boundaries

- Arabic-first, RTL-capable, accessible for children aged 6–12.
- Educational and communication support only; never present as diagnosis or therapy.
- Build a text-first Android MVP before optional speech/sign features.
- Do not store raw child audio/video by default. Prefer synthetic or de-identified data and minimize collection, retention, and logging.
- Make uncertain AI behavior explicit. Provide safe fallback responses and a documented route to caregiver/specialist support where appropriate.
- The activity sequence, permissions, safety policy, supported sign vocabulary, and completion criteria are deterministic. LLMs only interpret/generate language within constraints; they do not choose access rights or infer hidden psychological states.
- Core scenarios/AAC work offline from a versioned reviewed content pack. If AI/network services fail, use scripted approved responses; never improvise unreviewed offline text.
- Request camera/microphone permission only when that feature opens. Keep child mode free of ads, purchases, external links, child push notifications, and behavioral analytics SDKs; review/list any other third-party SDK.
- Require specialist-reviewed content and adult-support wording. Before research involving children or a child-facing pilot, obtain applicable institutional ethics review, guardian consent, child-appropriate assent, and a safe facilitation protocol.
- Do not present engagement or task completion as proof of improved mental health. Do not infer psychological state from face, voice tone, sign use, retries, or engagement.

## Engineering practices

- Keep module boundaries explicit and document setup, inputs/outputs, ownership, and tests in each module README.
- Agree on API schemas and error behavior before parallel integration. The backend publishes OpenAPI early; see [API_INTEGRATION_GUIDELINES.md](API_INTEGRATION_GUIDELINES.md).
- Prefer small pull requests with focused scope, issue links, reproducible validation steps, and screenshots for UI changes.
- Add or update tests for behavior that is implemented. Keep AI safety and conversation checks deterministic; do not make CI depend on live LLM calls or secrets.
- Pin or constrain dependencies once each module has a real manifest; review licenses and platform requirements.
- Never commit generated build artifacts, credentials, restricted datasets, local databases, or private model weights.

## Cross-team definition of done

A change is ready when its acceptance criteria are met, relevant tests/checks pass, documentation and API contracts are updated, privacy/safety impacts are reviewed, and a teammate has approved the pull request. Cross-module changes should identify integration owners and how the combined flow was checked. Demonstrate mobile changes on a real device where relevant and produce integration builds at least fortnightly during active development.
