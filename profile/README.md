<div align="center">
  <img src="ohho-logo.svg" alt="OhhO Robotics Logo" width="200"/>
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

We utilize a **Dual-License Architecture** to foster community innovation while building a sustainable enterprise business. Our robotics, AI engines, and SDKs are permissively licensed (MIT/Apache 2.0) for universal reuse, while our full-stack SaaS UI operates under a "Source-Available" (BSL) model.

### 🧠 Core Platform
*   [**ohho-robotics.com**](https://github.com/ohho-robotics/ohho-robotics.com) - The **OhhO OS** Cloud Platform (Next.js). The central dashboard for Fleet management, Digital Twins, AI Training pipelines, and MCP server integrations. *(Source- not Available)*
*   [**ohho-sdk**](https://github.com/ohho-robotics/ohho-sdk) - The open standard NPM packages for our communication protocols (WebSerial, WebBluetooth, ROSBridge), MCP tools, and JSON schemas. *(MIT)*

### 🤖 Hardware Reference Architectures (Apache 2.0)
To prove the versatility of the OhhO architecture, we maintain reference meta-repositories for the industry's most popular robot form factors. Clone any of these to instantly spin up an OhhO-compatible robot via Docker:

*   [**OmniBot**](https://github.com/ohho-robotics/OmniBot) - The flagship mecanum-wheel mobile manipulator. Features 9-DOF LeRobot teleoperation and stitched Bird's-Eye-View (BEV) perception.
*   [**OhhO-Humanoid**](https://github.com/ohho-robotics/OhhO-Humanoid) - The bipedal reference architecture. Demonstrates whole-body control (WBC) and dual-arm mobile manipulation using SmolVLA.
*   [**OhhO-Quadruped**](https://github.com/ohho-robotics/ohho-quadrupud) - The 4-legged reference architecture. Showcases Isaac Lab Reinforcement Learning locomotion integrated with OpenVLA for semantic navigation.
*   [**OhhO-Drone**](https://github.com/ohho-robotics/OhhO-Drone) - The aerial robotics architecture. Integrates MAVLink and PX4 with the OhhO cloud for autonomous 3D spatial mapping and fleet swarm control.


### 📱 Client Apps (MIT)
*   [**OhhO-VR**](https://github.com/ohho-robotics/OhhO-VR) - Unity-based mixed-reality client for Meta Quest 3 teleoperation and spatial data collection.
*   [**ohho.apk**](https://github.com/ohho-robotics/ohho.apk) - Native Android mobile controller and telemetry viewer.

### 🧩 Open-Source Tools & Libraries (MIT)
*   [**ros2-bev-stitcher**](https://github.com/ohho-robotics/ros2-bev-stitcher) - Real-time Bird's-Eye View camera stitching for ROS 2.
*   [**yahboom-python-driver**](https://github.com/ohho-robotics/yahboom-python-driver) - Pure-Python protocol encoder/decoder for Yahboom expansion boards.
*   [**mecanum-kinematics**](https://github.com/ohho-robotics/mecanum-kinematics) - Modular math library for omnidirectional drive systems.

---

## 🚀 Get Started
The fastest way to experience the OhhO platform is to run a digital twin in simulation:

```bash
git clone https://github.com/ohho-robotics/OhhO-Humanoid.git
cd OhhO-Humanoid
docker compose -f docker-compose.sim.yml up -d
```

## 🤝 Contributing
We love open-source contributions! Whether you're integrating a new robot protocol into **OhhO Connect**, contributing an AI skill to **OhhO Market**, or fixing a bug in the documentation, your PRs are always welcome. 

## 💼 Enterprise (OhhO Forge)
Running a fleet of robots in production? We offer enterprise subscriptions for managed cloud-GPU training (OhhO Train), massive fleet telemetry orchestration (OhhO Fleet), and SOC2-compliant security reporting (OhhO Comply). [Contact us for access.](mailto:enterprise@ohho-robotics.com)
