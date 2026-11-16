# Security and privacy

MindBridge Kids supports children aged 6–12. Treat all child-related information as highly sensitive. The application is for communication and education support and is not diagnostic or therapeutic.

## Credentials

- Keep API keys, passwords, signing keys, access tokens, and production connection strings in environment variables or an approved secrets manager.
- Never commit `.env` files. Use `.env.example` for variable names and safe placeholders only.
- Rotate credentials immediately if they enter source control, an issue, a screenshot, or a log. Removing a leaked value in a later commit does not make it safe.
- Do not print secret values in CI logs. Use GitHub Actions secrets only when a workflow genuinely needs them.

## Child data and media

- Do not use real child data in development, test fixtures, demos, or issue attachments.
- Raw child audio and video must not be stored by default. Prefer on-device processing and ephemeral in-memory handling where feasible; document any exception, retention, access, and deletion behavior before implementation.
- Keep personal data out of logs, analytics, crash reports, screenshots, and model prompts unless explicitly approved and necessary.
- Do not commit local databases, raw audio/video, private datasets, annotations containing personal data, or model checkpoints. Check dataset provenance, consent conditions, licenses, and redistribution terms before use.
- Use synthetic or properly de-identified test data and document its source.

## Reporting a concern

Do not report a vulnerability or expose sensitive data in a public issue. Contact the project leader privately through an agreed team channel and share only the minimum details needed to reproduce the concern. The team should restrict access while investigating and record remediation without copying sensitive data into the repository.

## Safety boundary

Content and model behavior must not claim diagnosis or treatment. Escalation, age-appropriate language, safe fallback behavior, and caregiver/specialist boundaries require documented review. See [DEVELOPMENT_GUIDELINES.md](DEVELOPMENT_GUIDELINES.md).
