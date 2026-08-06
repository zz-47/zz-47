<div align="center">

<pre>
████████  ████████            ██     ██  ████████
      ██        ██            ██     ██       ███
     ██       ██  ████████  ████████      ███
    ██      ██                  ██     ███
   ██     ██                  ██    ███
████████  ████████                  ██    ███
</pre>

<h3><b>ZEESHAN KAYANI</b></h3>

<p><i>Independent Researcher · Systems Cryptographer · Edge AI Architect</i></p>

<p>
  <a href="https://github.com/zz-47"><img src="https://img.shields.io/github/followers/zz-47?style=for-the-badge&color=090d16&labelColor=0d1117&logo=github" alt="GitHub"/></a>
  <a href="https://www.linkedin.com/in/zeeshan-kayani-0a1459350/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://zenodo.org/records/21815214"><img src="https://img.shields.io/badge/Zenodo-10.5281%2Fzenodo.21815214-168DEE?style=for-the-badge&logo=zenodo&logoColor=white" alt="Zenodo DOI"/></a>
  <a href="https://gitlab.com"><img src="https://img.shields.io/badge/GitLab-Workspace-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white" alt="GitLab"/></a>
</p>

</div>

---

## ◈ RESEARCH FOCUS

I study the mathematics of Small Language Models the way an engineer must — derived from first principles, then **measured against the real checkpoint**, never assumed from a spec sheet. The work lives at the intersection of constrained hardware, zero-trust cryptography, and deterministic local inference.

---

## ◈ CURRENT RESEARCH PROGRAM

- **SLM internals, verified on real weights.** Attention math — dot-product geometry, `1/√d_k` scaling, RoPE rotations, GQA KV-cache memory — traced to exact layer and tensor shapes in real checkpoints such as SmolLM2-135M.
- **Low-rank decomposition.** LoRA studied at the weight level: SVD → rank selection → scale-out → deploy-time merging, all measured rather than assumed.
- **Steered decoding on CPU.** Constrained generation via logit masking on CPU-only runtimes — no GPU, no cloud dependency.
- **Zero-trust local inference.** AES-GCM authenticated state, tmpfs RAM-disk isolation, canary auditing, and zero telemetry as architectural invariants.

> Companion publication archived with a live DOI: **10.5281/zenodo.21815214**.

---

## ◈ ARCHITECTURE AT A GLANCE

```text
                        ┌───────────────────────────────┐
                        │     HEADLESS DEBIAN NODE      │
                        │  Proxmox VE / tmpfs RAM-Disks │
                        └───────────────┬───────────────┘
                                        │
            ┌───────────────────────────┴───────────────────────────┐
            ▼                                                     ▼
┌───────────────────────┐                             ┌───────────────────────┐
│      AEGIS VAULT      │                             │      SLM ENGINE       │
├───────────────────────┤                             ├───────────────────────┤
│ • AES-GCM Encryption  │                             │ • GGUF Quantization   │
│ • N-Gram Filtering    │                             │ • Memory-Mapped Load  │
│ • Canary File Audit   │                             │ • Context Truncation  │
└───────────┬───────────┘                             └───────────┬───────────┘
            │                                                     │
            └──────────────────────────┬──────────────────────────┘
                                       │
                                       ▼
                        ┌───────────────────────────────┐
                        │    MODEL CONTEXT PROTOCOL     │
                        │   Local Agentic Bridge / API  │
                        └───────────────────────────────┘
```

---

## ◈ R&D MATRIX

**01 · Edge SLM Optimization & Quantization**
- Memory-efficient SLM execution in low-bit GGUF (2–4 bit) under standard CPU constraints.
- Aggressive context truncation and tmpfs RAM-disk caching to isolate execution and prevent overflow on legacy hardware.

**02 · Applied Cryptography & Threat Engines**
- Modular Python security pipelines over Authenticated Encryption with Associated Data (AEAD) / AES-GCM.
- Ransomware canary detection and real-time input sanitization via N-gram overlap indexing and regex validation.

**03 · Agentic Protocol Bridges & Forensics**
- Model Context Protocol (MCP) ecosystems as secure, local bridges between isolated inference endpoints.
- Forensic data inspection implementing Benford's Law anomaly detection over tabular transaction distributions.

**04 · Bare-Metal Infrastructure & Orchestration**
- CLI-first, low-overhead environments: headless Debian, Proxmox VE, LXC container networks.
- Kernel tuning, disk partitioning, and volatile storage routing for deterministic, zero-telemetry operations.

---

## ◈ METHODOLOGY

```text
measured, not assumed   →  every claim traced to a real tensor
zero telemetry          →  no state leaves the node
lowest footprint        →  run first on the weakest machine
```

---

## ◈ SYSTEM & RESEARCH LOG

```gdb
[0x00_HOST]      : HP G10 EliteBook // Headless Debian 12 (Bookworm)
[0x01_VIRT]      : Proxmox VE • LXC Containerization • Docker Orchestration
[0x02_CRYPTO]    : AEAD • AES-GCM
[0x03_SECURITY]  : N-Gram Overlap Indexing • Canary Directory Auditing
[0x04_MODEL_R&D] : Low-Bit GGUF (2–4 bit) • Private RAG • Model Context Protocol
[0x05_DEVSPEC]   : C / C++ • Python • FastAPI • Flask • Bash • SQL

[STATUS: ALL CORE R&D SYSTEMS OPERATIONAL // ZERO TELEMETRY]
```

---

<div align="center">

<p>
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=zz-47&theme=react-dark&hide_border=true&area=true" width="100%" alt="Research activity graph"/>
</p>

<br/>

**STACK**

<p>
  <img src="https://img.shields.io/badge/C%2B%2B-Low_Overhead_Engine-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-R%26D%20%2F%20Inference-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-API%20Gateways-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-Data%20Pipelines-003B57?style=for-the-badge&logo=postgresql&logoColor=white"/>
  <br/>
  <img src="https://img.shields.io/badge/GGUF-2--4bit%20Quantization-black?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/MCP-Local%20Agentic%20Bridges-black?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Linux-tmpfs%20RAM-Disks-FCC624?style=for-the-badge&logo=linux&logoColor=black"/>
  <img src="https://img.shields.io/badge/GitLab-Ultimate%20Workspace-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white"/>
</p>

<br/>

`DETERMINISM · ZERO DATA LEAKAGE · LOW FOOTPRINT`

</div>
