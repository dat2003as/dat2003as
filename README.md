<div align="center">
  
# Hi, I'm Vo Quoc Dat


###  AI Engineer | Computer Vision | LLM & Multi-Agent Systems | Edge AI

<p align="center">
  <em>Building end-to-end AI systems — from optimizing CV models on embedded NPUs <br>
  to architecting multi-agent LLM chatbots with RAG and Text-to-SQL pipelines.</em>
</p>

[![](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/dat614943)
[![](https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail)](mailto:dat614943@gmail.com)
[![](https://img.shields.io/badge/GitHub-Portfolio-181717?style=for-the-badge&logo=github)](https://github.com/dat2003as)

</div>

---

## The Toolbox

<table>
  <tr>
    <td width="20%"><b>Category</b></td>
    <td width="80%"><b>Technologies</b></td>
  </tr>
  <tr>
    <td><b>LLM & Agent</b></td>
    <td>
      <img src="https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
      <img src="https://img.shields.io/badge/GPT--4.1--mini-412991?style=flat-square&logo=openai&logoColor=white" />
      <img src="https://img.shields.io/badge/Vanna_(Text--to--SQL)-FF6F00?style=flat-square" />
      <img src="https://img.shields.io/badge/Tool_Calling_Agent-9C27B0?style=flat-square" />
    </td>
  </tr>
  <tr>
    <td><b>RAG & Vector DB</b></td>
    <td>
      <img src="https://img.shields.io/badge/pgvector-336791?style=flat-square&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Hybrid_Search_(RRF)-1976D2?style=flat-square" />
      <img src="https://img.shields.io/badge/Embeddings_(1536d)-00897B?style=flat-square" />
      <img src="https://img.shields.io/badge/Faiss-00ADD8?style=flat-square" />
    </td>
  </tr>
  <tr>
    <td><b>Edge Hardware & NPU</b></td>
    <td>
      <img src="https://img.shields.io/badge/Orange_Pi_6-E95420?style=flat-square" />
      <img src="https://img.shields.io/badge/Rockchip_SDK-000000?style=flat-square&logo=c" />
      <img src="https://img.shields.io/badge/Jetson_Nano-76B900?style=flat-square&logo=nvidia" />
    </td>
  </tr>
  <tr>
    <td><b>Deep Learning & CV</b></td>
    <td>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
      <img src="https://img.shields.io/badge/YOLO_v8%2Fv11-00FFFF?style=flat-square" />
      <img src="https://img.shields.io/badge/Face_Rec_(MobileFaceNet)-4169E1?style=flat-square" />
      <img src="https://img.shields.io/badge/Person_Re--ID_(OSNet)-8A2BE2?style=flat-square" />
    </td>
  </tr>
  <tr>
    <td><b>Inference & Optimization</b></td>
    <td>
      <img src="https://img.shields.io/badge/TensorRT-76B900?style=flat-square&logo=nvidia" />
      <img src="https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square" />
      <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv" />
    </td>
  </tr>
  <tr>
    <td><b>Backend & Infrastructure</b></td>
    <td>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi" />
      <img src="https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
      <img src="https://img.shields.io/badge/ZeroMQ-DF0000?style=flat-square" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker" />
      <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka" />
    </td>
  </tr>
  <tr>
    <td><b>Languages</b></td>
    <td>
      <img src="https://img.shields.io/badge/Python_3-3776AB?style=flat-square&logo=python" />
      <img src="https://img.shields.io/badge/C++_(Embedded)-00599C?style=flat-square&logo=c%2B%2B" />
      <img src="https://img.shields.io/badge/SQL-CC2927?style=flat-square" />
      <img src="https://img.shields.io/badge/Shell_Scripting-4EAA25?style=flat-square&logo=gnu-bash" />
    </td>
  </tr>
</table>

---

## Engineering Highlights

### 1. Multi-Agent AI Chatbot for Shrimp Farming ([mebieco-ai-chatbot](https://github.com/dat2003as/mebieco-ai-chatbot))
> *Production LLM system combining RAG + Text-to-SQL across 4 data domains.*

* **The Challenge:** Build an intelligent chatbot that can answer questions from both unstructured documents (SOPs, guides) and structured databases (inventory, IoT sensors, farm operations) — all in Vietnamese, with strict data isolation per farm.
* **The Solution:** Architected a **multi-agent orchestrator** with 4 specialized tools: **RAG hybrid search** (pgvector cosine + BM25 FTS, fused via RRF), **Vanna Text-to-SQL** with domain auto-routing across 4 schemas, **real-time web scraping** (shrimp prices, weather), and **LLM knowledge**. Implemented RBAC, SQL guardrails (SELECT-only, injection blocking), farm isolation via RLS, and anti-hallucination rules.
* **The Impact:** Deployed system serving **4 user roles** across **4 data domains**, handling natural language queries over **500+ database tables** with sub-second response times. Zero data leakage between farms.

### 2. Embedded NPU Optimization Pipeline (Orange Pi)
> *Solving the bottleneck of running heavy detection models on limited embedded RAM.*

* **The Challenge:** The standard Orange Pi SDK yielded poor inference speeds (~2 FPS) for object detection, making real-time application impossible.
* **The Solution:** Reverse-engineered the **NOE SDK** to architect a custom `.cix` conversion pipeline. Rewrote inference logic to bypass standard Python overheads.
* **The Impact:** Boosted inference throughput by **250% (2 FPS to 12 FPS)**, enabling viable real-time edge deployment.

### 3. Low-Latency Distributed Vision System
> *Decoupling heavy AI processing from logic control.*

* **The Challenge:** Running Detection, Re-ID, and Business Logic in a single synchronous loop caused massive latency spikes on the edge device.
* **The Solution:** Designed an asynchronous pipeline using **ZeroMQ (Pub/Sub)** to decouple the Detection Logic workers from the main control loop. Implemented **MobileFaceNet** & **OSNet** embeddings optimized with **Faiss**.
* **The Impact:** Achieved **<100ms system latency**, mirroring professional ROS2 architectural patterns.

### 4. Gesture-Based Hardware Control Bridge
> *Translating Computer Vision into Physical Action.*

* **The Challenge:** Creating a stable, jitter-free interface between Python CV output and Arduino hardware without using heavy protocols.
* **The Solution:** Developed a real-time MediaPipe pipeline for 1-5 finger classification and engineered a lightweight **Serial Protocol** bridge.
* **The Impact:** Established **negligible latency** communication, allowing fluid real-time control of physical GPIO/LED arrays via hand gestures.

---

## Current Focus
* **LLM Engineering:** Multi-agent orchestration, RAG optimization, prompt engineering for production systems.
* **Robotics:** Deepening knowledge in **ROS2** (Navigation2, Control Stacks).
* **Architecture:** Hybrid Edge-Cloud systems — bridging on-device inference with cloud LLM pipelines.

---

<div align="center">
  <p>2025 Vo Quoc Dat — Building intelligence from the edge to the cloud.</p>
</div>
