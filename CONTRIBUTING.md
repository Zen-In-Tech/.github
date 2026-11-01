# Contributing

These rules apply to every Zen-In-Tech repository that has no CONTRIBUTING.md of its own.

## Workflow

1. Every change starts with an issue.
2. Create a short-lived branch from `main`: `<type>/<issue>-<short-name>`, for example `feat/42-csv-export` or `fix/57-login-redirect`.
3. Open a pull request into `main` and link the issue with `Closes #42`. Keep it small: one issue per PR.
4. Merge with **squash merge** once CI passes and the PR is reviewed. The branch is deleted after merge.

`main` is always releasable. Never push directly to `main`: every change goes through a pull request.

## Commit and PR titles

PR titles follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). The title becomes the squash commit message and the release note.

| Type | Use for |
|---|---|
| `feat:` | New feature |
| `fix:` | Bug fix |
| `docs:` | Documentation only |
| `refactor:` | Code change without behavior change |
| `test:` | Tests |
| `perf:` | Performance |
| `ci:`, `chore:` | Build, CI, dependencies, tooling |

Add a scope when it helps: `fix(auth): keep session after password reset`. Mark breaking changes with `!`: `feat(api)!: remove v1 endpoints`.

## Before opening a PR

- It builds, and tests pass locally.
- No secrets, keys or personal data in code, commits or logs. Variable names go to `.env.example`, values never do.
- README, docs and `.env.example` are updated if behavior or configuration changed.

## Releases

Releases use SemVer tags (`v1.2.0`). Release notes are generated from PR titles.

## Security

Do not open public issues for vulnerabilities. See [SECURITY.md](SECURITY.md).
