<div align="center">
  <img src="profile/ohho-logo.svg" alt="OhhO Robotics logo" width="200"/>
  <h1>OhhO Robotics</h1>
  <p>OHHO ROBOTICS LTD builds OhhO OS, the safe runtime for open robot hardware. OhhO OS is proprietary; our reference robot, <a href="https://github.com/ohho-robotics/ohho-omnibot">OmniBot</a>, is open source.</p>

  <a href="https://ohho-robotics.com">Website</a> ·
  <a href="https://www.linkedin.com/company/ohho-robotics/">LinkedIn</a> ·
  <a href="https://ohho-robotics.com/docs">Documentation</a> ·
  <a href="https://www.youtube.com/@varun.vaidhiya/videos">Demos</a>
</div>

---

## OmniBot

<a href="https://github.com/ohho-robotics/ohho-omnibot"><img src="https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/assets/PXL_20260505_121303728.jpg" width="49%" alt="OmniBot, photo from the OmniBot repository"/></a>
<a href="https://github.com/ohho-robotics/ohho-omnibot"><img src="https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/assets/PXL_20260505_121328008.jpg" width="49%" alt="OmniBot, second photo from the OmniBot repository"/></a>

[OmniBot](https://github.com/ohho-robotics/ohho-omnibot) ([Apache-2.0](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/LICENSE)) is the open-source reference robot and the open project of OHHO ROBOTICS LTD. Photos and short clips are in [`assets/`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/assets): [demo 1](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/assets/Omnibot_demo1.gif) and [demo 2](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/assets/Omnibot_demo2.gif). The [OmniBot README](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/README.md) documents the hardware (Raspberry Pi 5, Yahboom expansion board, SO-101 arm).

What the latest green [CI run](https://github.com/ohho-robotics/ohho-omnibot/actions/runs/36756309478) of [`.github/workflows/ci.yml`](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/.github/workflows/ci.yml) checked:

*   **CPU tests and ruff.** Pytest for [`mecanum-kinematics/tests`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/mecanum-kinematics/tests), [`yahboom-python-driver/tests`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/yahboom-python-driver/tests), [`ros2-bev-stitcher/tests`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/ros2-bev-stitcher/tests), and [`omnibot_arm/test`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-ros2/omnibot_arm/test), plus the learning, agent, and data engine tests under [`omnibot-ai-engines`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-ai-engines).
*   **colcon build and test.** [`src/`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/src) is the colcon workspace (symlinks to the ROS 2 packages). That job runs in the `ros:jazzy-ros-base-noble` container named in the workflow file.

What is in the tree:

*   [**omnibot-ros2**](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-ros2) — ROS 2 packages `omnibot_driver`, `omnibot_bringup`, `omnibot_navigation`, `omnibot_arm`, `omnibot_description`, and `omnibot_hybrid`. Launch files, including [`robot_with_joy.launch.py`](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/omnibot-ros2/omnibot_bringup/launch/robot_with_joy.launch.py) and [`perception.launch.py`](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/omnibot-ros2/omnibot_bringup/launch/perception.launch.py), are in [`omnibot_bringup/launch`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-ros2/omnibot_bringup/launch).
*   [**omnibot-ai-ros2**](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-ai-ros2) — ROS 2 packages `omnibot_vla`, `omnibot_lerobot` (including [`teleop_recorder_node.py`](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/omnibot-ai-ros2/omnibot_lerobot/omnibot_lerobot/teleop_recorder_node.py)), `omnibot_rl`, and `omnibot_orchestration`.
*   [**omnibot-ai-engines**](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-ai-engines) — Python packages `agent_engine`, `data_engine`, `learning_engine`, `lerobot_engine`, `rl_engine`, and `vla_engine`.
*   [**omnibot-digital-twin**](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-digital-twin) — configs, scripts, and world file [`omnibot_lab.sdf`](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/omnibot-digital-twin/worlds/omnibot_lab.sdf).
*   [**omnibot-vr**](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-vr) and [**omnibot-android**](https://github.com/ohho-robotics/ohho-omnibot/tree/main/omnibot-android) — client trees kept inside this repository. The standalone Quest and Android apps are proprietary.

## Libraries inside OmniBot

These are directories in [OmniBot](https://github.com/ohho-robotics/ohho-omnibot), not separate repositories. The CPU job linked above tests all three.

| Directory | What the code is |
|---|---|
| [`mecanum-kinematics`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/mecanum-kinematics) | Mecanum wheel kinematics (C++ header and a Python package). Apache-2.0 [`LICENSE`](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/mecanum-kinematics/LICENSE) in that directory. |
| [`ros2-bev-stitcher`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/ros2-bev-stitcher) | ROS 2 node that warps several cameras into one bird's-eye view. Tests are in [`tests/`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/ros2-bev-stitcher/tests). |
| [`yahboom-python-driver`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/yahboom-python-driver) | Serial protocol encoder/decoder for Yahboom expansion boards. Tests are in [`tests/`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/yahboom-python-driver/tests). |

## OhhO OS and the OhhO products (proprietary)

OhhO OS (the `ohho-os` engine), the OhhO SDK, the OhhO Pilot Quest app, the Android app, the OhhO Fleet console, OhhO Verified, and the quadruped, humanoid and drone tracks are proprietary software of OHHO ROBOTICS LTD. They live in private repositories and are licensed per robot model, per robot, or per site. For an evaluation licence or a demo, contact us via [ohho-robotics.com](https://ohho-robotics.com).

Earlier public versions of those repositories, up to each repository's `last-apache-2.0` tag, and the [`ohho-os` 1.1.2](https://pypi.org/project/ohho-os/1.1.2/) package were released under Apache-2.0 and stay under that licence. Later changes are not open source.

## Get started

CPU demo from the [OmniBot README](https://github.com/ohho-robotics/ohho-omnibot#quickstart-no-robot-no-gpu), using `ohho-os` 1.1.2 (the last Apache-2.0 release of OhhO OS). No robot, ROS install, or container is required:

```bash
pip install ohho-os==1.1.2
ohho doctor
ohho sim --robot omnibot --seconds 2
```

In OmniBot, [`src/`](https://github.com/ohho-robotics/ohho-omnibot/tree/main/src) is the colcon workspace. The [colcon job](https://github.com/ohho-robotics/ohho-omnibot/actions/runs/36756309478) builds that path.

## Contributing

Outside contributions are welcome in [OmniBot](https://github.com/ohho-robotics/ohho-omnibot), the open project. See [CONTRIBUTING.md](CONTRIBUTING.md), [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md), and [SECURITY.md](SECURITY.md).

This repository is [Apache-2.0](LICENSE), and so is OmniBot. Everything else from OHHO ROBOTICS LTD is proprietary. Vendored third-party code keeps its own licence (OmniBot [NOTICE](https://raw.githubusercontent.com/ohho-robotics/ohho-omnibot/main/NOTICE)).
