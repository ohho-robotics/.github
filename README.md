<div align="center">
  <img src="profile/ohho-logo.svg" alt="OhhO Robotics logo" width="200"/>
  <h1>OhhO Robotics</h1>
  <p>Open-source mobile manipulation. The robot you can inspect today is <a href="https://github.com/ohho-robotics/OmniBot">OmniBot</a>.</p>

  <a href="https://ohho-robotics.com">Website</a> ·
  <a href="https://www.linkedin.com/company/ohho-robotics/">LinkedIn</a> ·
  <a href="https://ohho-robotics.com/docs">Documentation</a> ·
  <a href="https://www.youtube.com/@varun.vaidhiya/videos">Demos</a>
</div>

---

## OmniBot

<a href="https://github.com/ohho-robotics/OmniBot"><img src="https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/assets/PXL_20260505_121303728.jpg" width="49%" alt="OmniBot, photo from the OmniBot repository"/></a>
<a href="https://github.com/ohho-robotics/OmniBot"><img src="https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/assets/PXL_20260505_121328008.jpg" width="49%" alt="OmniBot, second photo from the OmniBot repository"/></a>

[OmniBot](https://github.com/ohho-robotics/OmniBot) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/LICENSE)) is the public robot repository. Photos and short clips are in [`assets/`](https://github.com/ohho-robotics/OmniBot/tree/main/assets): [demo 1](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/assets/Omnibot_demo1.gif) and [demo 2](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/assets/Omnibot_demo2.gif). The [OmniBot README](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/README.md) documents the hardware (Raspberry Pi 5, Yahboom expansion board, SO-101 arm).

What the latest green [CI run](https://github.com/ohho-robotics/OmniBot/actions/runs/36756309478) of [`.github/workflows/ci.yml`](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/.github/workflows/ci.yml) checked:

*   **CPU tests and ruff.** Pytest for [`mecanum-kinematics/tests`](https://github.com/ohho-robotics/OmniBot/tree/main/mecanum-kinematics/tests), [`yahboom-python-driver/tests`](https://github.com/ohho-robotics/OmniBot/tree/main/yahboom-python-driver/tests), [`ros2-bev-stitcher/tests`](https://github.com/ohho-robotics/OmniBot/tree/main/ros2-bev-stitcher/tests), and [`omnibot_arm/test`](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ros2/omnibot_arm/test), plus the learning, agent, and data engine tests under [`omnibot-ai-engines`](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ai-engines).
*   **colcon build and test.** [`src/`](https://github.com/ohho-robotics/OmniBot/tree/main/src) is the colcon workspace (symlinks to the ROS 2 packages). That job runs in the `ros:jazzy-ros-base-noble` container named in the workflow file.

What is in the tree:

*   [**omnibot-ros2**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ros2) — ROS 2 packages `omnibot_driver`, `omnibot_bringup`, `omnibot_navigation`, `omnibot_arm`, `omnibot_description`, and `omnibot_hybrid`. Launch files, including [`robot_with_joy.launch.py`](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/omnibot-ros2/omnibot_bringup/launch/robot_with_joy.launch.py) and [`perception.launch.py`](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/omnibot-ros2/omnibot_bringup/launch/perception.launch.py), are in [`omnibot_bringup/launch`](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ros2/omnibot_bringup/launch).
*   [**omnibot-ai-ros2**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ai-ros2) — ROS 2 packages `omnibot_vla`, `omnibot_lerobot` (including [`teleop_recorder_node.py`](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/omnibot-ai-ros2/omnibot_lerobot/omnibot_lerobot/teleop_recorder_node.py)), `omnibot_rl`, and `omnibot_orchestration`.
*   [**omnibot-ai-engines**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ai-engines) — Python packages `agent_engine`, `data_engine`, `learning_engine`, `lerobot_engine`, `rl_engine`, and `vla_engine`.
*   [**omnibot-digital-twin**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-digital-twin) — configs, scripts, and world file [`omnibot_lab.sdf`](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/omnibot-digital-twin/worlds/omnibot_lab.sdf).
*   [**omnibot-vr**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-vr) and [**omnibot-android**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-android) — client trees kept inside this repository. The standalone repos are below.

## ohho-sdk

[ohho-sdk](https://github.com/ohho-robotics/ohho-sdk) is OhhO OS: the Python package [`ohho-os`](https://pypi.org/project/ohho-os/) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/LICENSE)). [`pyproject.toml`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/pyproject.toml) sets `name = "ohho-os"` and `version = "1.1.2"`. The [v1.1.2 release run](https://github.com/ohho-robotics/ohho-sdk/actions/runs/36844693250) completed successfully, and the [1.1.2 project page](https://pypi.org/project/ohho-os/1.1.2/) is the published distribution.

```bash
pip install ohho-os
ohho doctor
ohho sim --robot omnibot --seconds 2
```

`ohho doctor` and `ohho sim --robot omnibot --seconds 2` are the CLI smoke steps in [`.github/workflows/ci.yml`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/.github/workflows/ci.yml). The latest [CI run on main](https://github.com/ohho-robotics/ohho-sdk/actions/runs/36842316506) succeeded.

The TypeScript workspace under [`ts/`](https://github.com/ohho-robotics/ohho-sdk/tree/main/ts) is not published to npm. [`ts/package.json`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/package.json) sets `"private": true`.

*   [`@ohho/connect`](https://github.com/ohho-robotics/ohho-sdk/tree/main/ts/packages/connect) — adapter sources [`webserial.ts`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/connect/src/webserial.ts), [`webbluetooth.ts`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/connect/src/webbluetooth.ts), [`rosbridge.ts`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/connect/src/rosbridge.ts), and [`yahboom.ts`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/connect/src/yahboom.ts).
*   [`@ohho/schemas`](https://github.com/ohho-robotics/ohho-sdk/tree/main/ts/packages/schemas) — schema sources. [`package.json`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/schemas/package.json) depends on `zod`.
*   [`@ohho/mcp`](https://github.com/ohho-robotics/ohho-sdk/tree/main/ts/packages/mcp) — MCP tool modules and [`registry.ts`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/mcp/src/registry.ts).
*   [`@ohho/client`](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/ts/packages/client/src/api.ts) — `OhhOClient` is an empty class.

## OhhO-VR

[OhhO-VR](https://github.com/ohho-robotics/OhhO-VR) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/OhhO-VR/main/LICENSE)) is a Unity project (`Assets`, `Packages`, and `ProjectSettings` at the repo root). Its [README](https://raw.githubusercontent.com/ohho-robotics/OhhO-VR/main/README.md) documents a Meta Quest teleop client for OmniBot over ROSBridge. Vendored packages keep their own licences ([NOTICE](https://raw.githubusercontent.com/ohho-robotics/OhhO-VR/main/NOTICE)).

## ohho.apk

[ohho.apk](https://github.com/ohho-robotics/ohho.apk) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/ohho.apk/main/LICENSE)) is a Kotlin Gradle project. Its [README](https://raw.githubusercontent.com/ohho-robotics/ohho.apk/main/README.md) documents an Android ROSBridge controller for OmniBot and which on-screen values are demo data. [Android CI](https://raw.githubusercontent.com/ohho-robotics/ohho.apk/main/.github/workflows/android-ci.yml) runs `./gradlew assembleDebug test`. The latest [run on main](https://github.com/ohho-robotics/ohho.apk/actions/runs/36583451280) succeeded.

## Concept — not started

[ohho-humanoid](https://github.com/ohho-robotics/ohho-humanoid), [ohho-quadruped](https://github.com/ohho-robotics/ohho-quadruped), and [ohho-drone](https://github.com/ohho-robotics/ohho-drone) are **concept — not started**. Each README says the repository does not contain a robot stack, and there is no quick-start command for them.

*   [ohho-humanoid](https://raw.githubusercontent.com/ohho-robotics/ohho-humanoid/main/README.md) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/ohho-humanoid/main/LICENSE))
*   [ohho-quadruped](https://raw.githubusercontent.com/ohho-robotics/ohho-quadruped/main/README.md) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/ohho-quadruped/main/LICENSE))
*   [ohho-drone](https://raw.githubusercontent.com/ohho-robotics/ohho-drone/main/README.md) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/ohho-drone/main/LICENSE))

## Libraries inside OmniBot

These are directories in [OmniBot](https://github.com/ohho-robotics/OmniBot), not separate repositories. The CPU job linked above tests all three.

| Directory | What the code is |
|---|---|
| [`mecanum-kinematics`](https://github.com/ohho-robotics/OmniBot/tree/main/mecanum-kinematics) | Mecanum wheel kinematics (C++ header and a Python package). Apache-2.0 [`LICENSE`](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/mecanum-kinematics/LICENSE) in that directory. |
| [`ros2-bev-stitcher`](https://github.com/ohho-robotics/OmniBot/tree/main/ros2-bev-stitcher) | ROS 2 node that warps several cameras into one bird's-eye view. Tests are in [`tests/`](https://github.com/ohho-robotics/OmniBot/tree/main/ros2-bev-stitcher/tests). |
| [`yahboom-python-driver`](https://github.com/ohho-robotics/OmniBot/tree/main/yahboom-python-driver) | Serial protocol encoder/decoder for Yahboom expansion boards. Tests are in [`tests/`](https://github.com/ohho-robotics/OmniBot/tree/main/yahboom-python-driver/tests). |

## Get started

CPU demo from [ohho-sdk CI](https://raw.githubusercontent.com/ohho-robotics/ohho-sdk/main/.github/workflows/ci.yml). No robot, ROS install, or container is required:

```bash
pip install ohho-os
ohho doctor
ohho sim --robot omnibot --seconds 2
```

In OmniBot, [`src/`](https://github.com/ohho-robotics/OmniBot/tree/main/src) is the colcon workspace. The [colcon job](https://github.com/ohho-robotics/OmniBot/actions/runs/36756309478) builds that path.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md), [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md), and [SECURITY.md](SECURITY.md).

This repository is [Apache-2.0](LICENSE). The public repositories linked above are Apache-2.0; each Apache-2.0 link points at that repository's `LICENSE` file. Vendored third-party code keeps its own licence (OhhO-VR [NOTICE](https://raw.githubusercontent.com/ohho-robotics/OhhO-VR/main/NOTICE), OmniBot [NOTICE](https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/NOTICE)).
