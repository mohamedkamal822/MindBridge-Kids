# Mobile app (planned)

**Owner:** M4 (Flutter architecture and integration) with M5 (RTL UI/UX and accessibility).

This planned Flutter module will provide Arabic-first communication practice, social scenarios, emotional-awareness activities, visual/AAC message composition, caregiver access, and offline content. It is a support and education tool, not diagnosis or therapy. Android is first; iOS is a later feasibility target. No mobile application has been scaffolded yet.

## Product constraints to preserve

- Arabic RTL throughout; decide numeral conventions with specialist input. Use short language, optional read-aloud, screen-reader labels, scalable text, reduced motion, and touch targets of at least 48 dp.
- One task per scenario screen; always offer a hint/“try another way,” no time pressure, and a visible “I need a grown-up” action on every child screen.
- Review composed/transcribed input before sending. Speech transcription must be correctable; child can bypass speech. Sign capture must show a camera-on indicator, supported vocabulary and confidence retry, with AAC fallback.
- Core text/cards/scenarios work offline using a bundled versioned content pack and reviewed scripted responses. Queue only minimal task events for later sync.
- Ask for camera/microphone permission only when the feature opens, explain it plainly, and make the app usable without either permission. Do not persist raw media by default.
- Parent gate protects caregiver/settings, consent, and deletion areas. No ads, purchases, external links, behavioral analytics SDKs, or push notifications to child mode.
- Caregiver summaries separate observed task outcomes from interpretation; no hidden scores or psychological inference.

## Setup

When the owners define the first vertical slice, add the Flutter project and document the pinned Flutter/Dart versions, Android device/toolchain setup, optional iOS setup, environment configuration, and exact `flutter pub get`, `flutter analyze`, and `flutter test` commands here. The minimum OS remains undecided until the Month 1 device survey. Use OS secure storage for tokens and SQLite for the approved local content pack; define any other persisted fields explicitly.
