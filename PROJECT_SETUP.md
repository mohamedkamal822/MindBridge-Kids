# Project setup

## Current repository state

The repository currently starts with the project README and Flutter-oriented ignore rules. Mobile, backend, AI, data, safety, and test modules are planned but are not scaffolded yet. Add a module when there is implementation work and a maintainer; CI skips modules without their manifests.

## Prerequisites by module

Install tools only for the module you are contributing to:

- Mobile: Flutter SDK and Android toolchain; verify installation with `flutter doctor`. Survey target devices and choose the minimum OS in Month 1. Android is first; iOS depends on feasibility and available build/signing access.
- Backend: Python 3.11 or the version declared by the backend manifest, plus PostgreSQL when the implementation requires it.
- AI/research: use the Python version and dependencies declared by that module; follow dataset/model license and privacy requirements.
- Git and a GitHub account with repository access.

## Contributor checkout

```bash
git clone https://github.com/mohamedkamal822/MindBridge-Kids.git
cd MindBridge-Kids
git switch main
git pull --ff-only origin main
```

After the project leader creates `develop`, update your local refs and create work branches from it as described in [GIT_WORKFLOW.md](GIT_WORKFLOW.md).

## Module setup

When a module lands, its owner must document exact installation, environment variables, start/run commands, migrations (where relevant), and checks in that module’s README. Keep real values in ignored `.env` files and copy names/placeholders from `.env.example`. Do not invent secrets or commit local environment files. For mobile, document device/OS support, parent-gate and permission setup, bundled offline content, and on-device versus remote data flows. Initial distribution is internal/pilot (APK/TestFlight if available); public app-store release is outside the current project scope.

## Initial project bootstrap

The first month should deliver requirements and architecture, repository/CI setup, dataset/license audit, and a scenario taxonomy. Create real module scaffolding only after its owner defines the first vertical slice. The backend should publish the OpenAPI contract in month two, early enough for mobile and AI teams to build against it independently.
