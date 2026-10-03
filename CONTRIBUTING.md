# Contributing

OhhO Robotics is a small public GitHub organization. The code a contributor can actually open is listed below.

## Where to send a change

| Repository | What it is |
|---|---|
| [OmniBot](https://github.com/ohho-robotics/OmniBot) | ROS 2 workspace, AI packages, digital-twin notes, and the mecanum, BEV, and Yahboom directories |
| [ohho-sdk](https://github.com/ohho-robotics/ohho-sdk) | OhhO OS: Python package [`ohho-os`](https://pypi.org/project/ohho-os/) on PyPI. TypeScript sources under [`ts/packages/`](https://github.com/ohho-robotics/ohho-sdk/tree/main/ts/packages) are a private workspace (`@ohho/client` is an empty class) |
| [OhhO-VR](https://github.com/ohho-robotics/OhhO-VR) | Unity project for Quest teleop |
| [ohho.apk](https://github.com/ohho-robotics/ohho.apk) | Kotlin Android project |
| [ohho-robotics/.github](https://github.com/ohho-robotics/.github) | This organization profile and the default community files |

[ohho-humanoid](https://github.com/ohho-robotics/ohho-humanoid), [ohho-quadruped](https://github.com/ohho-robotics/ohho-quadruped), and [ohho-drone](https://github.com/ohho-robotics/ohho-drone) are **Concept — not started**. They do not contain a buildable robot stack. Please do not open feature work against them until there is code to build.

## Pull requests

1. Fork the repository you are changing and open a pull request against `main`.
2. The org-default template ([.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md)) asks for what changed, how to run it, and evidence (a CI run, a test, or a dated video, trial CSV, MCAP, or dataset). Fill that in. A repository with its own template keeps that file instead.
3. Do not add a public claim (a feature marked as working, a license, a compliance badge, or a "clone and run" command) unless the pull request links to the code, a CI run, or a recording that shows it.

## Showcase rule

A feature moves to Built on the live site only when all four are true. The [public roadmap](https://ohho-robotics.com/roadmap) (page not live yet) lists Built, In progress, and Vision.

1. **Merged.** The code is on `main` of a public `ohho-robotics` repository. Private code does not count.
2. **Runnable.** A stranger can run it from the README in 15 minutes or less (sim or laptop). If it needs hardware, the page says "needs hardware" and links a dated video plus logs or bag files.
3. **Evidenced.** At least one of: a green CI run that exercises the feature, a test file, or a dated video, trial CSV, MCAP file, or dataset URL.
4. **Copy matches the evidence.** Every number (tests, latency, success rate, version) comes from code or CI output. Do not use adjectives the evidence does not support ("production-ready", "any robot", "real-time", "enterprise").

Anything else is In progress (an open Linear issue or pull request, and a target month) or Vision (no code yet; always labelled "Vision: not built", only on the roadmap or a product page's Vision section). A demo alone never counts: an in-browser console on simulated data stays "Interactive demo · simulated data".

Do not publish, including as vision: logo, partner, insurer, or vendor walls; customer, fleet, or "in the field" claims; prices or paid plans; certification, "compliant", or DoC claims; team size, roles, or volunteer asks; AI-generated footage that is not labelled "Concept render — not footage of OmniBot" (the caption the site uses).

## License

OhhO's public repositories are Apache-2.0. Vendored third-party code keeps its own license.

## Conduct

This organization uses the [Contributor Covenant](CODE_OF_CONDUCT.md). Report security issues using [SECURITY.md](SECURITY.md), not a public issue.
