<div align="center">
  
# Vo Quoc Dat
### Edge AI Engineer | NPU Optimization Specialist

<p align="center">
  <em>Specializing in optimizing Computer Vision models for embedded constraints (Rockchip/Orange Pi). Focused on converting heavy Deep Learning models into real-time edge solutions by bridging the gap between Python research and Hardware deployment.</em>
</p>

[![](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/dat614943)
[![](https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail)](mailto:dat614943@gmail.com)

</div>

---

## 🛠 The Toolbox: Hardware & AI Integration

My stack focuses on the entire pipeline: from model training to quantization and bare-metal deployment.

| **Category** | **Technologies** |
| :--- | :--- |
| **Edge Hardware & NPU** | ![Orange Pi](https://img.shields.io/badge/Orange_Pi_6-E95420?style=flat-square) ![Rockchip](https://img.shields.io/badge/Rockchip_SDK-000000?style=flat-square&logo=c) ![NVIDIA](https://img.shields.io/badge/Jetson_Nano-76B900?style=flat-square&logo=nvidia) |
| **Computer Vision Core** | ![YOLO](https://img.shields.io/badge/YOLO_v8%2Fv11-00FFFF?style=flat-square) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv) ![MediaPipe](https://img.shields.io/badge/MediaPipe-00B140?style=flat-square) ![ONNX](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square) |
| **Backend & Messaging** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi) ![ZeroMQ](https://img.shields.io/badge/ZeroMQ-DF0000?style=flat-square) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka) |
| **Languages & Systems** | ![Python](https://img.shields.io/badge/Python_3-3776AB?style=flat-square&logo=python) ![Linux](https://img.shields.io/badge/Ubuntu_Linux-FCC624?style=flat-square&logo=linux) ![Shell](https://img.shields.io/badge/Shell_Scripting-4EAA25?style=flat-square&logo=gnu-bash) |

---

## 🚀 Engineering Highlights

### 1. Embedded NPU Optimization Pipeline (Orange Pi)
> *Solving the bottleneck of running heavy detection models on limited embedded RAM.*

* **The Challenge:** The standard Orange Pi SDK yielded poor inference speeds (~2 FPS) for object detection, making real-time application impossible.
* **The Solution:** Reverse-engineered the **NOE SDK** to architect a custom `.cix` conversion pipeline. Rewrote inference logic to bypass standard Python overheads.
* **The Impact:** ⚡ **Boosted inference throughput by 250% (2 FPS → 12 FPS)**, enabling viable real-time edge deployment.

### 2. Low-Latency Distributed Vision System
> *Decoupling heavy AI processing from logic control.*

* **The Challenge:** Running Detection, Re-ID, and Business Logic in a single synchronous loop caused massive latency spikes on the edge device.
* **The Solution:** Designed an asynchronous pipeline using **ZeroMQ (Pub/Sub)** to decouple the Detection Logic workers from the main control loop. Implemented **MobileFaceNet** & **OSNet** embeddings via **Faiss**.
* **The Impact:** ⏱ Achieved **<100ms system latency**, mirroring professional ROS2 architectural patterns.

### 3. Gesture-Based Hardware Control Bridge
> *Translating Computer Vision into Physical Action.*

* **The Challenge:** Creating a stable, jitter-free interface between Python CV output and Arduino hardware without using heavy protocols.
* **The Solution:** Developed a real-time MediaPipe pipeline for 1-5 finger classification and engineered a lightweight **Serial Protocol** bridge.
* **The Impact:** 🤖 Established **negligible latency** communication, allowing fluid real-time control of physical GPIO/LED arrays via hand gestures.

---

## 🔭 Current Focus
I am currently transitioning from pure embedded optimization to full robotics orchestration.
* **Learning:** **ROS2** (Navigation & Control Stacks).
* **Exploring:** Advanced C++ optimizations for bare-metal performance.

---

<div align="center">
  <p>© 2025 Vo Quoc Dat. Building intelligence at the edge.</p>
</div>
