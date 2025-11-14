# GO HW — From Models to Systems  
### Unified Graph Runtime for Logic, AI, Hardware & Energy  
**Whitepaper v1.3**

---

## 📘 Introduction

GO HW extends ONNX far beyond traditional inference by transforming a model into a **fully deployable system** capable of orchestrating:

- logic and real-time control  
- sensors and actuators  
- DMA transfers and synchronization signals  
- energy constraints and timing behavior  
- multi-hardware execution (CPU, GPU, FPGA, SoC, NPU…)

The objective is clear: **unify Logic + AI + Hardware** under a single executable, portable, energy-aware graph.

This whitepaper introduces the foundations of this paradigm shift, describing how an ONNX graph evolves from a model into a complete hardware-driven pipeline.

---

## 🧭 Table of Contents (short overview)

- Vision and motivation  
- ONNX in plain language  
- ONNX Runtime today  
- IR-last → IR-first transition  
- Limitations of current approaches  
- Introduction to the GO HW Runtime  
- Unified orchestration  
- Hardware control & system signals  
- Compilation, pipelines and EPs  
- GO HW roadmap  

---

# 🧩 1. Global Vision  
### Unifying AI + Logic + Hardware + Energy

The industry suffers from extreme fragmentation: proprietary SDKs, inconsistent APIs, multiple execution layers, and no shared representation for hardware control or real-time behavior.

GO HW introduces a **single graph abstraction** that can simultaneously:

- interact with GPIO, ADC, DAC, PWM  
- schedule DMA transfers  
- handle timers, triggers and synchronization  
- execute inference  
- manage energy and latency  
- deploy across hardware targets without vendor SDKs  

The graph becomes the **orchestration language** for the entire system.

---

# 📈 2. The GO HW Quadrant  
### Positioning the unified graph runtime

![GO HW Quadrant](./GO%20HW%20%E2%80%94%20From%20Models%20to%20Systems/GO-HW_Orvillechart.png)

GO HW sits in the “disruptive” zone by enabling:

- **10+ hardware targets from one graph**  
- **deployment in under 10 minutes**  
- **±2% energy precision**  
- **<5% timing jitter**  
- **0 vendor dependency**  
- **100% abstraction, no SDKs needed**  

This positions GO HW as a universal orchestration layer across CPUs, GPUs, FPGAs and SoCs.

---

# ⚙️ 3. Internal Architecture  
### IR-last today, IR-first tomorrow

![IR Pipeline](./GO%20HW%20%E2%80%94%20From%20Models%20to%20Systems/IR.png)

GO HW adopts a hybrid architecture:

### 🔹 IR Last  
The current ONNX Runtime pipeline:  
graph optimization → EP → hardware execution.

### 🔹 IR First (MLIR / IREE / OpenXLA)  
The upcoming GO HW extension:  
ahead-of-time compilation, full graph fusion, deterministic memory planning and unified pipelines for logic + AI + hardware.

This transition unlocks tighter hardware integration while maintaining ONNX’s portability.

---

# 🔌 4. Hardware I/O, DMA and signals embedded directly in the graph

GO HW introduces **new hardware-aware ONNX operators**, including:

- `GPIO.Read`, `GPIO.Write`  
- `ADC.Read`, `DAC.Write`  
- `DMA.Transfer`  
- `Timer.Start`, `Timer.Wait`  
- `Trigger.Rise`, `Sync.Wait`  
- `Energy.Profile`, `Energy.Limit`

These nodes transform the graph into a **system-level orchestrator**, enabling unified control of:

- sensors and actuators  
- DMA and shared memory  
- real-time loops  
- inference engines  
- energy and thermal constraints  

The entire system becomes graph-described, portable and reproducible.

---

# 🖥️ 5. Direct Hardware Deployment  
### The graph *is* the program

With GO HW:

- an ONNX graph becomes a **standalone hardware executable**,  
- vendor SDKs (CUDA, Vitis, QNN, OpenVINO…) are no longer required,  
- the runtime manages memory, DMA, synchronization and timing,  
- the same graph deploys seamlessly across CPU, GPU, FPGA, SoC, NPU.

Deployment becomes drastically simpler and integration costs fall significantly.

---

# 🧪 6. Visual Excerpts from the Whitepaper

### Cover  
![Cover](./img/GO-HW_Whitepaper.PNG)

### IR & Orchestration  
![IR](./img/IR.png)

### Strategic Quadrant  
![Quadrant](./img/Orvillechart.png)

---

# 🚀 7. Industrial Impact

GO HW targets domains where the convergence of AI, control and hardware is essential:

- advanced automation  
- robotics and embedded vision  
- energy & smart infrastructure  
- aerospace & defense  
- test benches and instrumentation  
- embedded & edge computing  

The unified graph approach reduces:

- integration delays  
- engineering complexity  
- long-term maintenance costs  
- vendor lock-in  

---

# 📄 8. Download the Whitepaper

👉 **[GO HW — From Models to Systems (Whitepaper v1.3)](./GO%20HW%20%E2%80%94%20From%20Models%20to%20Systems/GO-HW_Whitepaper_1.3.pdf)**

---

If you need a marketing-oriented version, a more technical deep-dive, or a website-ready HTML page, I can generate those as well.
