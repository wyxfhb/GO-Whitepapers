<p align="center">
  <img src="./GO-HW_Whitepaper.PNG" alt="GO HW Cover" width="720">
</p>

# GO HW — From Models to Systems  
### Unified Graph Runtime for Logic, AI, Hardware & Energy  
**Whitepaper v1.3**

---

## Introduction

GO HW extends ONNX far beyond traditional inference by transforming a model into a **fully deployable system** that orchestrates:

- logic and real-time control  
- sensors and actuators  
- DMA transfers and synchronization signals  
- energy constraints and timing behavior  
- multi-hardware execution (CPU, GPU, FPGA, SoC, NPU…)

The goal is simple: **unify Logic + AI + Hardware** under a single executable, portable, energy-aware graph.

This whitepaper presents how an ONNX model evolves from a static file into a full hardware-driven system.

---

## Table of Contents (overview)

- Vision and motivation  
- ONNX explained simply  
- ONNX Runtime today  
- IR-last → IR-first transition  
- Limitations of current frameworks  
- The GO HW runtime  
- Unified orchestration  
- Hardware control nodes  
- Compilation & execution flow  
- Roadmap  

---

# 1. Global Vision  
### Unifying AI, logic, hardware and energy

Current industrial pipelines are fragmented: proprietary SDKs, inconsistent APIs, and multiple incompatible runtimes.  
GO HW introduces a **single graph abstraction** capable of:

- interacting with GPIO, ADC, DAC, PWM  
- triggering DMA transfers  
- handling timers and synchronization  
- executing AI models  
- managing energy and timing  
- deploying to many hardware targets without vendor SDKs  

The graph becomes a **complete orchestration language**.

---

# 2. The GO HW Quadrant  
### Positioning the unified graph runtime

<p align="center">
  <img src="./GO-HW_Orvillechart.png" alt="Quadrant" width="720">
</p>

GO HW enters the “disruptive zone” with:

- **10+ hardware targets from a single graph**  
- **deployment under 10 minutes**  
- **±2% energy precision**  
- **<5% timing jitter**  
- **0 vendor dependency**  
- **100% abstraction**  

---

#  3. Internal Architecture  
### IR-last today, IR-first tomorrow

<p align="center">
  <img src="./IR.png" alt="IR Pipeline" width="720">
</p>

GO HW uses a hybrid architecture:

### 🔹 IR Last  
Current ONNX Runtime flow: optimization → EP → execution.

### 🔹 IR First (MLIR / IREE / OpenXLA)  
Future approach:  
AOT compilation, memory planning, fusion of logic + AI + hardware, deterministic timing.

This unlocks a deeper hardware integration while keeping ONNX portability.

---

# 4. Hardware I/O, DMA and signal control in the graph

GO HW introduces new hardware-aware ONNX operators such as:

- `GPIO.Read`, `GPIO.Write`  
- `ADC.Read`, `DAC.Write`  
- `DMA.Transfer`  
- `Timer.Start`, `Timer.Wait`  
- `Trigger.Rise`, `Sync.Wait`  
- `Energy.Profile`, `Energy.Limit`

These nodes turn the graph into a **system-level orchestrator**, capable of unified control over:

- sensors & actuators  
- real-time pipelines  
- inference  
- DMA and shared memory  
- energy & thermal constraints  

---

# 🖥️ 5. Direct Hardware Deployment  
### The graph becomes the program

With GO HW:

- an ONNX file becomes a **portable hardware executable**,  
- vendor SDKs (CUDA, Vitis, QNN, OpenVINO…) are no longer required,  
- the runtime manages synchronization, memory, DMA, timing,  
- the same graph deploys seamlessly on CPU, GPU, FPGA, SoC, NPU.

This drastically simplifies deployment while reducing long-term integration costs.

---

# 6. Industrial Impact

GO HW is designed for domains where AI + control + hardware integration matters:

- robotics & embedded vision  
- advanced automation  
- energy & smart infrastructure  
- aerospace & defense  
- instrumentation & test benches  
- embedded & edge AI  

The unified graph approach reduces:

- integration complexity  
- development costs  
- vendor lock-in  
- hardware-specific rewrites  

---

# Download the Whitepaper

👉 **[GO HW — From Models to Systems (Whitepaper v1.4 PDF)](./GO-HW_Whitepaper_1.4.pdf)**

---
