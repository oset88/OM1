![OM_Banner_X2 (1)](https://github.com/user-attachments/assets/853153b7-351a-433d-9e1a-d257b781f93c)

<p align="center">  
  <a href="https://arxiv.org/abs/2412.18588">Technical Paper</a> |  
  <a href="https://docs.openmind.org/">Documentation</a> |  
  <a href="https://x.com/openmind_agi">X</a> |  
  <a href="https://discord.gg/VUjpg4ef5n">Discord</a>  
</p>

---

# OpenMind OM1

**OM1 is a modular AI runtime that empowers developers to create and deploy multimodal AI agents across digital environments and physical robots**, including Humanoids, Phone Apps, websites, Quadrupeds, and educational robots such as TurtleBot 4.  

OM1 agents can process diverse inputs like web data, social media, camera feeds, and LIDAR, while enabling physical actions including motion, autonomous navigation, and natural conversations.  

The goal of OM1 is to make it easy to create highly capable human-focused robots, that are easy to upgrade and (re)configure to accommodate different physical form factors.

---

## 🚀 Capabilities of OM1

- **Modular Architecture**: Designed with Python for simplicity and seamless integration.  
- **Data Input**: Easily handles new data and sensors.  
- **Hardware Support via Plugins**: Supports new hardware through plugins for API endpoints and specific robot hardware connections to `ROS2`, `Zenoh`, and `CycloneDDS`. (We recommend `Zenoh` for all new development).  
- **Web-Based Debugging Display**: Monitor the system in action with WebSim (http://localhost:8000/).  
- **Pre-configured Endpoints**: Built-in support for Voice-to-Speech, OpenAI’s `gpt-4o`, DeepSeek, and multiple Visual Language Models (VLMs).  

---

## 🏗️ Architecture Overview

![Architecture](https://github.com/user-attachments/assets/14e9b916-4df7-4700-9336-2983c85be311)

---

## 🖐 Getting Started - Hello World

The simplest demo is the **Spot agent**. Spot uses your webcam to capture and label objects. These text captions are then sent to `OpenAI 4o`, which returns `movement`, `speech` and `face` action commands. These commands are displayed on WebSim with basic timing and debugging info.

---

### 🔹 Package Management and VENV

You will need the [`uv` package manager](https://docs.astral.sh/uv/getting-started/installation/).  
💡 *`uv` is a modern Python package manager that replaces pip/venv with faster and simpler workflows.*

---

### 🔹 Clone the Repo

```bash
git clone https://github.com/openmind/OM1.git
cd OM1
git submodule update --init
uv venv
