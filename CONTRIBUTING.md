# Contributing

## Before you start

- Read the project [setup](PROJECT_SETUP.md), [team ownership](TEAM_STRUCTURE.md), [development guidance](DEVELOPMENT_GUIDELINES.md), and [API integration rules](API_INTEGRATION_GUIDELINES.md).
- Pick a GitHub issue, confirm its deliverable and acceptance criteria, and coordinate with its owning team.
- Do not include identifiable child data, credentials, raw recordings, or unlicensed datasets in issues, commits, or pull requests.

## Branch and pull request workflow

`main` contains reviewed, tested releases. `develop` is the integration branch. Work on short-lived `feature/*`, `fix/*`, or `docs/*` branches and submit pull requests to `develop`. Never develop directly on `main` or push directly to `develop`; do not force-push shared branches. The detailed flow is in [GIT_WORKFLOW.md](GIT_WORKFLOW.md).

```bash
git clone https://github.com/mohamedkamal822/MindBridge-Kids.git
cd MindBridge-Kids
git switch main
git pull --ff-only origin main
git switch -c feature/short-task-name
# make a focused change, then run the checks relevant to that module
git add <files>
git commit -m "feat: describe the change"
git push -u origin feature/short-task-name
```

Once `develop` exists, start feature branches from it:

```bash
git fetch origin
git switch develop
git pull --ff-only origin develop
git switch -c feature/short-task-name
```

Use conventional prefixes where useful: `feat:`, `fix:`, `docs:`, `test:`, `refactor:`, `chore:`. Keep commits and pull requests focused, link the issue with `Closes #<number>`, explain how the change was checked, and include screenshots for UI changes.

## Review and merge requirements

- Target `develop`; only approved releases target `main`.
- Request at least one review from a teammate, ideally someone from the affected integration boundary.
- Resolve review conversations and ensure required CI checks pass before merging.
- Never merge a failing or unreviewed pull request. Keep secrets out of CI logs and repository history.

Branch protection is a repository setting and must be enabled manually by a repository admin; see [GIT_WORKFLOW.md](GIT_WORKFLOW.md).
