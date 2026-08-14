<p align="center">
  <img src="banner.jpg" width="100%" alt="banner"/>
</p>

<div align="center">

<a href="https://www.linkedin.com/in/zeeshan-kayani-0a1459350/"><img src="https://img.shields.io/badge/LinkedIn-CONNECT-0d1117?style=for-the-badge&logo=linkedin&logoColor=0A66C2" alt="LinkedIn"/></a>
<a href="https://zenodo.org/records/21815214"><img src="https://img.shields.io/badge/Zenodo-10.5281%2Fzenodo.21815214-0d1117?style=for-the-badge&logo=zenodo&logoColor=168DEE" alt="Zenodo DOI"/></a>
<a href="https://gitlab.com"><img src="https://img.shields.io/badge/GitLab-WORKSPACE-0d1117?style=for-the-badge&logo=gitlab&logoColor=FC6D26" alt="GitLab"/></a>
<a href="https://github.com/zz-47"><img src="https://img.shields.io/badge/GitHub-zz--47-0d1117?style=for-the-badge&logo=github&logoColor=ffffff" alt="GitHub"/></a>

<br/>

<img src="https://img.shields.io/badge/C%2B%2B-LOW_LEVEL-0d1117?style=for-the-badge&logo=cplusplus&logoColor=00599C"/>
<img src="https://img.shields.io/badge/Python-R%26D_%2F_INFERENCE-0d1117?style=for-the-badge&logo=python&logoColor=3776AB"/>
<img src="https://img.shields.io/badge/FastAPI-API_GATEWAYS-0d1117?style=for-the-badge&logo=fastapi&logoColor=009688"/>
<img src="https://img.shields.io/badge/PostgreSQL-DATA_PIPELINES-0d1117?style=for-the-badge&logo=postgresql&logoColor=336791"/>
<br/>
<img src="https://img.shields.io/badge/Debian-HEADLESS_12-0d1117?style=for-the-badge&logo=debian&logoColor=A81D33"/>
<img src="https://img.shields.io/badge/Linux-tmpfs_RAM_DISKS-0d1117?style=for-the-badge&logo=linux&logoColor=FCC624"/>
<img src="https://img.shields.io/badge/GGUF-2--4_BIT_QUANT-0d1117?style=for-the-badge"/>
<img src="https://img.shields.io/badge/MCP-LOCAL_BRIDGES-0d1117?style=for-the-badge"/>

</div>

---

## Research Focus

I perform case studies on mathematics and concepts behind Small Language Models — derived from first principles, then **measured against the real checkpoint**, never assumed from a spec sheet. The work sits at the intersection of constrained hardware, zero-trust cryptography, and deterministic local inference.

---

## Current Research

- **SLM internals on real weights** — attention math (`1/√d_k` scaling, RoPE rotations, GQA KV-cache), traced to exact layer and tensor shapes in real checkpoints such as SmolLM2-135M.
- **Low-rank decomposition** — LoRA at the weight level: SVD → rank selection → scale-out → deploy-time merging, measured rather than assumed.
- **Steered decoding on CPU** — constrained generation via logit masking on CPU-only runtimes; no GPU, no cloud dependency.
- **Zero-trust local inference** — AES-GCM authenticated state, tmpfs RAM-disk isolation, canary auditing, and zero telemetry as architectural invariants.

---

## System Topology

<details>
<summary><b>Research node — headless Debian topology</b></summary>

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

</details>

---

## R&D Matrix

**01 · Edge SLM Optimization & Quantization** — low-bit GGUF (2–4 bit) execution under standard CPU constraints; context truncation and tmpfs RAM-disk caching to isolate execution on legacy hardware.

**02 · Applied Cryptography & Threat Engines** — AEAD / AES-GCM security pipelines; ransomware canary detection and input sanitization via N-gram overlap indexing and regex validation.

**03 · Agentic Protocol Bridges & Forensics** — Model Context Protocol (MCP) as secure local bridges between isolated inference endpoints; Benford's Law anomaly detection over tabular transaction data.

**04 · Bare-Metal Infrastructure & Orchestration** — headless Debian, Proxmox VE, and LXC container networks; kernel tuning and volatile storage routing for deterministic, zero-telemetry operation.

---

## Publication

A research archive is recorded under a live DOI:

<a href="https://zenodo.org/records/21815214"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21815214-0d1117?style=flat-square&logo=zenodo&logoColor=168DEE" alt="Zenodo DOI"/></a>

---

## Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=zz-47&theme=react-dark&hide_border=true&area=true" width="100%" alt="Activity graph"/>

<br/>

<code>DETERMINISM · ZERO DATA LEAKAGE · LOW FOOTPRINT</code>

</div>
