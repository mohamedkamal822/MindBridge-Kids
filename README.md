# MindBridge Kids

Arabic-first communication, social-practice, and emotional-awareness activities for children aged 6–12. The plan combines a Flutter app, FastAPI backend, a deterministic activity engine, constrained conversational AI/RAG, offline AAC/scenario packs, and evaluated optional speech/sign input.

> MindBridge Kids is an educational and communication support project. It is not diagnostic or therapeutic, and must not infer psychological states. Optional speech and sign recognition must not delay the text-first core MVP.

## Repository status

This repository is being prepared for a seven-member graduation project. At setup time, it contains the starter README and Flutter `.gitignore`; application modules, API contracts, and tests have not yet been added. The CI workflows skip modules that do not yet exist.

## Planned layout

```text
mobile/                         Flutter application (M4, M5)
backend/                        FastAPI, PostgreSQL, API contract (M3)
ai/                             Arabic conversation, intent and RAG (M1)
intelligent-inputs/
  sign-recognition/              Sign research and evaluation (M2)
  speech-and-data/               Speech benchmarks and data register (M6)
safety/                          Safety requirements and review
tests/                           Integration and cross-module tests (M7)
docs/                            Architecture, API, requirements and plans
.github/                         CI, issue forms and contribution templates
```

Directories should be added alongside real work. Don’t create empty applications or move existing work without a reviewed migration plan.

## Start here

1. Read [PROJECT_SETUP.md](PROJECT_SETUP.md) and [TEAM_STRUCTURE.md](TEAM_STRUCTURE.md).
2. Follow [CONTRIBUTING.md](CONTRIBUTING.md) and [GIT_WORKFLOW.md](GIT_WORKFLOW.md).
3. Pick a task from [docs/requirements/STARTER_BACKLOG.md](docs/requirements/STARTER_BACKLOG.md) or open a GitHub issue.
4. The backend team should publish the OpenAPI contract early; see [API_INTEGRATION_GUIDELINES.md](API_INTEGRATION_GUIDELINES.md). Candidate datasets, benchmark targets, evaluation metrics, and license checks are documented in [the data/content plan](docs/requirements/DATA_AND_CONTENT_PLAN.md).

## Project timeline

The eight-month plan and first-month priorities are in [docs/requirements/ROADMAP.md](docs/requirements/ROADMAP.md). The core MVP is a text-first Android experience; speech and sign modules require an evidence-based go/no-go decision.

## Development and safety

See [DEVELOPMENT_GUIDELINES.md](DEVELOPMENT_GUIDELINES.md), [SECURITY.md](SECURITY.md), and [docs/architecture/README.md](docs/architecture/README.md). Never commit credentials, private child data, raw audio/video, sensitive datasets, local databases, or private model checkpoints. Raw child audio and video must not be stored by default.
