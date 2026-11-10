# Contributing

Thanks for taking the time to contribute. These guidelines apply to every
repository under this account unless a repository ships its own
`CONTRIBUTING.md`.

## Before you start

- **Search existing issues.** The bug may already be tracked, or a fix may
  already be in flight.
- **Open an issue first for anything non-trivial.** A short design note saves
  everyone from building the wrong thing. Small fixes can go straight to a
  pull request.
- **One topic per issue.** Mixed reports get closed and reopened, which loses
  history.

## Development setup

Most projects in this account are TypeScript-first.

```bash
npm ci
npm run dev
```

Some repositories ship a frontend and an API side by side:

```bash
# API (NestJS + Prisma)
cd Backend
npm ci
npx prisma generate
npm run dev

# Web (Next.js)
cd Frontend
npm ci
npm run dev
```

Copy the example environment files before the first run, and never commit a
real `.env` file.

## Ground rules

| Rule | Why |
| --- | --- |
| Never commit secrets | `.env` files, API keys and certificates are ignored and must stay that way |
| No `.env` in a PR | Even a placeholder with a real-looking value gets the branch blocked |
| TypeScript strict | `npm run type-check` must pass |
| Tests for new logic | A PR without a test gets asked for one |
| Small, reviewable diffs | A 2,000-line PR is a 2,000-line review nobody does |
| One logical change per commit | History is documentation |

## Commit style

Use [Conventional Commits](https://www.conventionalcommits.org/):

```text
feat: add scheduled post-to-blog sync
fix: prevent duplicate slug on re-publish
docs: clarify deployment runbook
refactor: extract engagement scoring into a service
```

## Pull requests

1. Branch from `main` with a descriptive name: `feat/scheduled-sync`.
2. Make sure the checks pass locally:
   ```bash
   npm run build
   npm test
   npm run type-check
   ```
3. Fill in the pull request template: what changed, why, how it was verified.
4. Link the issue it closes (`Closes #123`).
5. CI must be green before review.

## Reporting a security issue

**Do not open a public issue for a vulnerability.** Follow the process in
[SECURITY.md](SECURITY.md) instead.

## Code of conduct

Participation is governed by [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## License

Contributions are licensed under the MIT License, the same license as the
repository you contribute to.
