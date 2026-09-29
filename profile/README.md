<div align="center">
  <img src="ohho-logo.svg" alt="OhhO Robotics logo" width="200"/>
  <h1>OhhO Robotics</h1>
  <p>Open-source mobile manipulation. The robot you can inspect today is <a href="https://github.com/ohho-robotics/OmniBot">OmniBot</a>.</p>

  <a href="https://ohho-robotics.com">Website</a> ·
  <a href="https://ohho-robotics.com/docs">Documentation</a> ·
  <a href="https://www.youtube.com/@varun.vaidhiya/videos">Demos</a>
</div>

---

## OmniBot

<a href="https://github.com/ohho-robotics/OmniBot"><img src="https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/assets/PXL_20260505_121303728.jpg" width="49%" alt="OmniBot, photo from the OmniBot repository"/></a>
<a href="https://github.com/ohho-robotics/OmniBot"><img src="https://raw.githubusercontent.com/ohho-robotics/OmniBot/main/assets/PXL_20260505_121328008.jpg" width="49%" alt="OmniBot, second photo from the OmniBot repository"/></a>

[OmniBot](https://github.com/ohho-robotics/OmniBot) is the public meta-repository: ROS 2 code, photos, and the client trees. Short clips from that repo: [demo 1](https://github.com/ohho-robotics/OmniBot/blob/main/assets/Omnibot_demo1.gif) and [demo 2](https://github.com/ohho-robotics/OmniBot/blob/main/assets/Omnibot_demo2.gif). The [OmniBot README](https://github.com/ohho-robotics/OmniBot/blob/main/README.md) documents the hardware (Raspberry Pi 5, Yahboom expansion board, SO-101 arm) and a YouTube channel.

What is in the tree:

*   [**omnibot-ros2**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ros2) — ROS 2 packages `omnibot_driver`, `omnibot_bringup`, `omnibot_navigation`, `omnibot_arm`, `omnibot_description`, and `omnibot_hybrid`. Launch files, including `robot_with_joy.launch.py` and `perception.launch.py`, are in [`omnibot_bringup/launch`](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ros2/omnibot_bringup/launch).
*   [**omnibot-ai-ros2**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ai-ros2) — ROS 2 packages including `omnibot_vla`, `omnibot_lerobot` (with `teleop_recorder_node.py`), `omnibot_rl`, and `omnibot_orchestration`.
*   [**omnibot-ai-engines**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-ai-engines) — Python packages `agent_engine`, `data_engine`, `learning_engine`, `lerobot_engine`, `rl_engine`, and `vla_engine`.
*   [**omnibot-digital-twin**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-digital-twin) — simulation notes and world files in that directory.
*   [**omnibot-vr**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-vr) and [**omnibot-android**](https://github.com/ohho-robotics/OmniBot/tree/main/omnibot-android) — client trees kept inside this meta-repository. The standalone repos are listed below.

## ohho-sdk

[ohho-sdk](https://github.com/ohho-robotics/ohho-sdk) is a TypeScript workspace. `package.json` sets `"private": true`. These packages are not published to npm.

*   [`@ohho/connect`](https://github.com/ohho-robotics/ohho-sdk/tree/main/packages/connect) — source for WebSerial, WebBluetooth, ROSBridge, and Yahboom adapters (`packages/connect/src`).
*   [`@ohho/schemas`](https://github.com/ohho-robotics/ohho-sdk/tree/main/packages/schemas) — Zod schema modules.
*   [`@ohho/mcp`](https://github.com/ohho-robotics/ohho-sdk/tree/main/packages/mcp) — MCP tool modules and a registry.
*   [`@ohho/client`](https://github.com/ohho-robotics/ohho-sdk/blob/main/packages/client/src/api.ts) — **Roadmap.** `OhhOClient` is an empty class.

## OhhO-VR

[OhhO-VR](https://github.com/ohho-robotics/OhhO-VR) is a Unity project (`Assets`, `Packages`, `ProjectSettings` at the repo root). Its README documents a Meta Quest teleop client for OmniBot over ROSBridge.

## ohho.apk

[ohho.apk](https://github.com/ohho-robotics/ohho.apk) is a Kotlin Gradle project. Its README documents an Android ROSBridge controller for OmniBot.

## Concept — not started

These repositories are a README, a compose file, and an `ohho.repos` manifest. They do not contain a robot stack. The compose images and the Git repositories named in `ohho.repos` are not published, so there is no quick-start command here.

*   [ohho-humanoid](https://github.com/ohho-robotics/ohho-humanoid)
*   [ohho-quadruped](https://github.com/ohho-robotics/ohho-quadruped)
*   [ohho-drone](https://github.com/ohho-robotics/ohho-drone)

## Libraries inside OmniBot

These are directories in [OmniBot](https://github.com/ohho-robotics/OmniBot), not separate repositories.

| Directory | What the code is |
|---|---|
| [`mecanum-kinematics`](https://github.com/ohho-robotics/OmniBot/tree/main/mecanum-kinematics) | Mecanum wheel kinematics (C++ header and a Python mirror). This directory has an Apache-2.0 `LICENSE` file. |
| [`ros2-bev-stitcher`](https://github.com/ohho-robotics/OmniBot/tree/main/ros2-bev-stitcher) | ROS 2 node that warps several cameras into one bird's-eye view. |
| [`yahboom-python-driver`](https://github.com/ohho-robotics/OmniBot/tree/main/yahboom-python-driver) | Serial protocol encoder/decoder for Yahboom expansion boards, with a ROS 2 driver. |

The other OmniBot directories (`omnibot-ros2`, `omnibot-ai-ros2`, `omnibot-ai-engines`, `omnibot-digital-twin`) are linked above. None of them is its own GitHub repository.

## Get Started

```bash
git clone https://github.com/ohho-robotics/OmniBot.git
cd OmniBot
```

ROS 2 packages live in `omnibot-ros2/` (there is no `src/` directory). The [OmniBot README](https://github.com/ohho-robotics/OmniBot/blob/main/README.md) documents Ubuntu 24.04 and ROS 2 Jazzy as the target for those packages.

## Contributing

See [CONTRIBUTING.md](../CONTRIBUTING.md), [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md), and [SECURITY.md](../SECURITY.md).

Public repositories do not yet have a top-level `LICENSE` file, except the Apache-2.0 file inside `OmniBot/mecanum-kinematics`. Do not assume a license for the rest.
