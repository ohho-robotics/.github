# Contributing

OHHO ROBOTICS LTD has one open project: [OmniBot](https://github.com/ohho-robotics/ohho-omnibot) (Apache-2.0). That is where outside contributions go.

## Where to send a change

| Repository | What it is |
|---|---|
| [ohho-omnibot](https://github.com/ohho-robotics/ohho-omnibot) | OmniBot: ROS 2 workspace, AI packages, digital-twin notes, and the mecanum, BEV, and Yahboom directories |
| [ohho-robotics/.github](https://github.com/ohho-robotics/.github) | This organization profile and the default community files |

OhhO OS, the OhhO SDK, the Quest and Android apps, the console, and the quadruped, humanoid and drone tracks are proprietary and live in private repositories. They do not accept outside contributions. OmniBot talks to OhhO OS only through public interfaces; see the boundary section in the [OmniBot README](https://github.com/ohho-robotics/ohho-omnibot#boundary-with-ohho-os).

## Pull requests

1. Fork the repository you are changing and open a pull request against `main`.
2. The org-default template ([.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md)) asks for what changed, how to run it, and evidence (a CI run, a test, or a dated video, trial CSV, MCAP, or dataset). Fill that in. A repository with its own template keeps that file instead.
3. Do not add a public claim (a feature marked as working, a license, a compliance badge, or a "clone and run" command) unless the pull request links to the code, a CI run, or a recording that shows it.
4. Sign off every commit (see [Developer Certificate of Origin](#developer-certificate-of-origin)).

## Developer Certificate of Origin

Every commit must be signed off (`git commit -s`). The sign-off adds a `Signed-off-by: Your Name <email>` line and certifies the [Developer Certificate of Origin 1.1](https://developercertificate.org/): you wrote the change, or have the right to submit it under the repository's licence.

Contributions to the open repositories are accepted under their licence (Apache-2.0, section 5). You keep the copyright in your contribution. There is no contributor licence agreement (CLA).

To sign off commits you already made: `git commit --amend -s` for the last commit, or `git rebase --signoff main` for a branch.

## Showcase rule

A feature moves to Built on the live site only when all four are true. The [public roadmap](https://ohho-robotics.com/roadmap) (page not live yet) lists Built, In progress, and Vision.

1. **Merged.** The code is on `main` of an `ohho-robotics` repository. For a private repository, the evidence in point 3 must be something we can show (a CI run summary, a dated video, or logs).
2. **Runnable.** A stranger (or, for proprietary code, an evaluation licensee) can run it from the README in 15 minutes or less (sim or laptop). If it needs hardware, the page says "needs hardware" and links a dated video plus logs or bag files.
3. **Evidenced.** At least one of: a green CI run that exercises the feature, a test file, or a dated video, trial CSV, MCAP file, or dataset URL.
4. **Copy matches the evidence.** Every number (tests, latency, success rate, version) comes from code or CI output. Do not use adjectives the evidence does not support ("production-ready", "any robot", "real-time", "enterprise").

Anything else is In progress (an open Linear issue or pull request, and a target month) or Vision (no code yet; always labelled "Vision: not built", only on the roadmap or a product page's Vision section). A demo alone never counts: an in-browser console on simulated data stays "Interactive demo · simulated data".

Do not publish, including as vision: logo, partner, insurer, or vendor walls; customer, fleet, or "in the field" claims; prices or paid plans; certification, "compliant", or DoC claims; team size, roles, or volunteer asks; AI-generated footage that is not labelled "Concept render — not footage of OmniBot" (the caption the site uses).

## License

OmniBot (`ohho-omnibot`) and this `.github` repository are Apache-2.0. All other OHHO ROBOTICS LTD software is proprietary (all rights reserved); earlier public versions up to each repository's `last-apache-2.0` tag stay under Apache-2.0. Vendored third-party code keeps its own license.

## Conduct

This organization uses the [Contributor Covenant](CODE_OF_CONDUCT.md). Report security issues using [SECURITY.md](SECURITY.md), not a public issue.
