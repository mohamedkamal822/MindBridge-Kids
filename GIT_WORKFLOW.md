# Git workflow and GitHub setup

## Branches

- `main`: stable, reviewed, tested release snapshots.
- `develop`: integration branch for the current milestone.
- `feature/<short-name>`: feature work, for example `feature/mobile-chat`, `feature/backend-auth`, `feature/ai-conversation`, `feature/sign-recognition`, `feature/aac-interface`.
- `fix/<short-name>`: bug fixes.
- `docs/<short-name>`: documentation changes.

All feature, fix, and documentation pull requests target `develop`. Only approved, tested releases move from `develop` to `main`. No direct development on `main`, no direct pushes to `develop`, and no force pushes to shared branches.

## First-time branch setup

An administrator should create `develop` from the initial `main` after reviewing this setup. This repository setup does not create or switch remote branches automatically.

```bash
git clone https://github.com/mohamedkamal822/MindBridge-Kids.git
cd MindBridge-Kids
git switch main
git pull --ff-only origin main
# After the admin creates develop:
git fetch origin
git switch --track origin/develop
```

## Daily feature flow

```bash
git switch develop
git pull --ff-only origin develop
git switch -c feature/your-short-task
# edit, run checks, commit
git add <files>
git commit -m "feat: explain the change"
git push -u origin feature/your-short-task
```

Open a pull request from the feature branch to `develop`. Link the issue, identify the team, explain testing and privacy implications, and request review. Merge only after review approval and all required checks pass. Delete the branch after merging. Release pull requests from `develop` to `main` require project-leader approval and a tested milestone.

## Recommended GitHub repository settings (manual)

In **Settings → Branches**, add rulesets or protection rules for `main` and `develop`:

- Require pull requests before merging, with at least one approval.
- Dismiss stale approvals when new commits are pushed; require approval of the latest reviewable push if available.
- Require status checks to pass before merging once the CI checks have run at least once.
- Require conversation resolution.
- Block force pushes and branch deletion on protected branches.
- Restrict direct pushes to `main`; restrict `develop` to pull-request merges.

Set up the GitHub Project named **MindBridge Kids – Development Tracker** using [the board plan](docs/requirements/PROJECT_BOARD.md). Apply documented labels in [docs/requirements/LABELS.md](docs/requirements/LABELS.md). Assign accounts only after members provide their GitHub usernames.
