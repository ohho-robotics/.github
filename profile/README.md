<div align="center">
  <img src="https://raw.githubusercontent.com/ohho-robotics/ohho-robotics.com/main/public/ohho-logo.svg" alt="OhhO Robotics Logo" width="200"/>
  <h1>Welcome to OhhO Robotics 🤖</h1>
  <p><strong>Building the Open-Source Standard for Embodied AI & Mobile Manipulation</strong></p>
  
  <a href="https://ohho-robotics.com">Website</a> •
  <a href="https://ohho-robotics.com/docs">Documentation</a> •
  <a href="https://discord.gg/ohhorobotics">Discord Community</a>
</div>

---

## 🌍 About Us
At **OhhO Robotics**, we are democratizing embodied AI. We build the foundational open-source ecosystem that allows anyone—from students to enterprise factories—to simulate, train, and operate AI-driven robots at scale. 

Our flagship platform bridges the gap between hardware control (ROS 2) and modern foundation models (OpenVLA, SmolVLA, LeRobot), giving robots the ability to see, think, and interact with the physical world.

---

## 🛠️ The OhhO Ecosystem

We have modularized our architecture so you can adopt the entire platform or just the specific packages you need for your own robots.

### 🧠 Core Platform
*   [**ohho-robotics.com**](https://github.com/ohho-robotics/ohho-robotics.com) - The **OhhO OS** Cloud Platform (Next.js). The central dashboard for Fleet management, Digital Twins, AI Training pipelines, and MCP server integrations.
*   [**OmniBot**](https://github.com/ohho-robotics/OmniBot) - The complete reference architecture and meta-repository. Clone this to spin up a fully functioning AI robot via Docker in minutes.

### 🦾 Robotics & AI Engines
*   [**omnibot-ros2**](https://github.com/ohho-robotics/omnibot-ros2) - The foundational ROS 2 Jazzy workspace (navigation, SLAM, kinematics, arm control).
*   [**omnibot-ai-ros2**](https://github.com/ohho-robotics/omnibot-ai-ros2) - The ROS 2 wrappers linking physical hardware to AI foundation models.
*   [**omnibot-ai-engines**](https://github.com/ohho-robotics/omnibot-ai-engines) - Pure Python/FastAPI backend servers for OpenVLA inference, RL training, and LeRobot episode data collection.
*   [**omnibot-digital-twin**](https://github.com/ohho-robotics/omnibot-digital-twin) - High-fidelity Gazebo and Isaac Sim environments.

### 📱 Client Apps
*   [**OhhO-VR**](https://github.com/ohho-robotics/OhhO-VR) - Unity-based mixed-reality client for Meta Quest 3 teleoperation and spatial data collection.
*   [**ohho.apk**](https://github.com/ohho-robotics/ohho.apk) - Native Android mobile controller and telemetry viewer.

### 🧩 Open-Source Tools & Libraries
*   [**ros2-bev-stitcher**](https://github.com/ohho-robotics/ros2-bev-stitcher) - Real-time Bird's-Eye View camera stitching for ROS 2.
*   [**yahboom-python-driver**](https://github.com/ohho-robotics/yahboom-python-driver) - Pure-Python protocol encoder/decoder for Yahboom expansion boards.
*   [**mecanum-kinematics**](https://github.com/ohho-robotics/mecanum-kinematics) - Modular math library for omnidirectional drive systems.

---

## 🚀 Get Started
The fastest way to experience the OhhO platform is to run the digital twin in simulation:

```bash
git clone https://github.com/ohho-robotics/OmniBot.git
cd OmniBot
docker compose -f docker-compose.sim.yml up -d
```

## 🤝 Contributing
We love open-source contributions! Whether you're integrating a new robot protocol into **OhhO Connect**, contributing an AI skill to **OhhO Market**, or fixing a bug in the documentation, your PRs are always welcome. Check out the `CONTRIBUTING.md` file in any of our repositories.

## 💼 Enterprise (OhhO Forge)
Running a fleet of robots in production? We offer enterprise subscriptions for managed cloud-GPU training (OhhO Train), massive fleet telemetry orchestration (OhhO Fleet), and SOC2-compliant security reporting (OhhO Comply). [Contact us for access.](mailto:enterprise@ohho-robotics.com)
