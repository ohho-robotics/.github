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
2. Describe what changed and how you checked it.
3. Do not add a public claim (a feature marked as working, a license, a compliance badge, or a "clone and run" command) unless the pull request links to the code, a CI run, or a recording that shows it.

## License

OhhO's public repositories are Apache-2.0. Vendored third-party code keeps its own license.

## Conduct

This organization uses the [Contributor Covenant](CODE_OF_CONDUCT.md). Report security issues using [SECURITY.md](SECURITY.md), not a public issue.
