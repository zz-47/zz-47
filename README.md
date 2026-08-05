<div align="center">

# Zeeshan Kayani
**Independent Researcher & Edge AI Engineer**  
*Constrained Inference Systems • Applied Cryptography • Local Infrastructure*

<br/>

<!-- Shields Row -->
[![GitHub Followers](https://img.shields.io/github/followers/zz-47?style=for-the-badge&color=0d1117&labelColor=161b22&logo=github)](https://github.com/zz-47)
[![Status](https://img.shields.io/badge/Focus-Private_AI_%2F_Edge-0d1117?style=for-the-badge&labelColor=161b22&logo=target)](https://github.com/zz-47)
[![License](https://img.shields.io/badge/License-MIT-0d1117?style=for-the-badge&labelColor=161b22&logo=open-source-initiative)](https://opensource.org/licenses/MIT)

<br/>

### 🛠️ Languages & Technical Stack

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" />
  <br/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Debian-A80033?style=for-the-badge&logo=debian&logoColor=white" />
  <img src="https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" />
</p>

</div>

---

### 🔬 Core Architecture & Research

```
  ┌─────────────────────────────────────────────────────────┐
  │                   LOCAL EDGE INFERENCE                  │
  │  ┌───────────────┐     ┌───────────────┐     ┌───────┐  │
  │  │  Debian/LXC   │ ──> │ GGUF (2-4 bit)│ ──> │  SLM  │  │
  │  └───────────────┘     └───────────────┘     └───────┘  │
  └────────────────────────────┬────────────────────────────┘
                               │
                               ▼
  ┌─────────────────────────────────────────────────────────┐
  │               CRYPTOGRAPHIC CANARY VAULT                │
  │  ┌───────────────┐     ┌───────────────┐     ┌───────┐  │
  │  │ N-Gram Index  │ ──> │    AES-GCM    │ ──> │ Audit │  │
  │  └───────────────┘     └───────────────┘     └───────┘  │
  └─────────────────────────────────────────────────────────┘
```

#### **1. Edge Inference Pipeline (`slm-engine`)**
* Built memory-mapped local loading logic using low-bit GGUF quantizations for low-overhead CPUs.
* Implemented context-truncation strategies to prevent memory overflow on legacy hardware.

#### **2. Cryptographic Canary Vault (`Aegis Vault`)**
* Modular Python security engine utilizing AES-GCM AEAD primitives.
* Features real-time directory integrity checks and input sanitization pipelines via regex and N-gram overlap indexing.

#### **3. Forensic Data Pipeline**
* Autonomous multi-agent auditor using Benford's Law to analyze transaction distributions in CSV datasets for anomaly detection.

---

### 💻 System Specifications & Environment

```bash
# Target Infrastructure Metrics
OS         : Debian 12 (Bookworm) / Proxmox VE
Kernel     : Linux 6.x Headless
Deployment : LXC Containers / RAM-Disks (tmpfs)
Focus      : Low-Latency, Zero-Data-Leakage Local Processing
```

---

### 📊 Activity Metrics

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=zz-47&theme=react-dark&hide_border=true&area=true" width="100%" alt="Zeeshan's GitHub Activity" />
</p>

---

### 🤝 Private Consulting & Enterprise Deployments

I partner with agencies, SaaS providers, and technical teams to architect private AI solutions:

* **On-Premise Private RAG:** Secure, zero-telemetry internal vector search.
* **MCP Integration Workflows:** Bridging isolated LLM/SLM endpoints to live databases and local operational toolkits.
* **Legacy Resource Optimization:** Benchmarking and refactoring standard AI inference loads for low-spec server environments.

<div align="center">

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/zeeshan-kayani)
[![GitLab](https://img.shields.io/badge/GitLab-Hub-FC6D26?style=for-the-badge&logo=gitlab)](https://gitlab.com)

`Determinism • Zero Data Leakage • Low Footprint`

</div>
