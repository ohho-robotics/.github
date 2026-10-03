## Cursor Cloud specific instructions

This repository is the GitHub organization profile for OhhO Robotics (`ohho-robotics/.github`). Tracked content includes `README.md`, `profile/README.md` (the page GitHub renders as the org profile), `profile/ohho-logo.svg`, `.github/PULL_REQUEST_TEMPLATE.md` (the org-default pull request template; there is no second copy at the repo root), and `.lycheeignore` (skips only `https://ohho-robotics.com/roadmap` in the link check). There is no package manifest, lockfile, linter, test suite, build, or service to start. Dependency refresh on startup is a no-op.

The `docker compose -f docker-compose.sim.yml up -d` snippet in `README.md` belongs to the separate `OhhO-Humanoid` repository. That compose file is not in this checkout.

`profile/README.md` references `ohho-logo.svg` in the same directory, so the org profile logo resolves. The root `README.md` uses the same relative path, and the SVG file is only present under `profile/`.
