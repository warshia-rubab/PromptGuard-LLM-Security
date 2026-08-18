# 🛡️PromptGuard: Detection & Mitigation of Distributed Prompt Jailbreak Attacks on LLMs

## **Research Paper** · IEEE Format · NUTECH Islamabad · 2025

[![PDF](https://img.shields.io/badge/Paper-PDF-red)](./paper/IEEE_Research_Paper.pdf)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black)](https://github.com/warshia-rubab/PromptGuard-LLM-Security)
[![License](https://img.shields.io/badge/License-MIT-green)](./LICENSE)


# 📖 Abstract

Large Language Models (LLMs) face an escalating security threat from **distributed prompt jailbreak attacks**. In these scenarios, malicious actors bypass per-prompt safety filters by fracturing a harmful request across multiple independent sessions.

**PromptGuard** is a novel **three-stage pre-inference middleware architecture** designed to detect and neutralize these attacks before they reach the LLM.

---

# 🔬 Research Overview

### The Problem
- **Stateless Guardrails**: Current LLM safety filters judge each prompt in isolation
- **PDC Framework**: Achieved **73.2% bypass rate** against state-of-the-art protocols
- **MalwareBench**: **3,520 adversarial prompts** across 11 jailbreak methodologies
- **29 LLMs** tested — all vulnerable

### Our Solution: PromptGuard

| Stage | Component | Function |
|-------|-----------|----------|
| **1** | Syntactic Fragmentation Detection | Identifies incomplete clauses, dangling anaphors, and abrupt semantic shifts |
| **2** | Cross-Session Context Analyzer | SBERT embeddings + FAISS for multi-session threat detection |
| **3** | Intent Classification Engine | Fine-tuned DistilBERT trained on MalwareBench (29 categories) |

### Key Features
- ✅ **Model-Agnostic**: Works with ANY LLM API
- ✅ **Low Latency**: Target < 100ms processing
- ✅ **No Model Modifications**: Plug-and-play reverse proxy
- ✅ **Enterprise-Ready**: Compatible with OpenAI, Google, Anthropic APIs

---

# 📊 Evaluation Benchmarks

| Metric | Target |
|--------|--------|
| **F₁ Score** | ≥ 0.85 |
| **False Positive Rate** | < 5% |
| **Latency** | < 100ms (95th percentile) |
| **PDC Neutralization** | ≥ 80% |

---
# 🏗️ Architecture
User → Stage 1 → Stage 2 → Stage 3 → LLM API
↓
❌ Blocked


### Stage Details

| Stage | Component | Function |
|-------|-----------|----------|
| 1 | Structural Detection | Incomplete clauses, dangling anaphors, abrupt shifts |
| 2 | SBERT + FAISS | Multi-session tracking, cosine similarity |
| 3 | DistilBERT | MalwareBench classification (29 categories) |





## 📚 Research Context

| Framework | Contribution |
|-----------|-------------|
| **PDC Framework** (Waireus et al., 2025) | Demonstrated 73.2% bypass rate for distributed attacks |
| **MalwareBench** (Li et al., 2025) | 3,520 adversarial prompts across 11 jailbreak methodologies |
| **Zou et al.** (2023) | Universal adversarial suffixes (single-prompt focus) |

### Our Contribution
PromptGuard is the **first middleware-driven defense** explicitly engineered to counter distributed prompt jailbreaks in live LLM API environments.

---


# 📁 Repository Structure

```
PromptGuard-LLM-Security/
├── README.md ← This file
├── LICENSE ← MIT License
├── paper/
│ └── IEEE_Research_Paper.pdf ← Full research paper
├── figures/
│ ├── fig1.png ← Attack workflow diagram
│ ├── flowchart.png ← Comparative analysis
│ ├── flowchart_alt.png ← Defense architecture
│ └── image.png ← Project timeline
└── tables/
└── table.png ← Evaluation metrics

```

---

# 📝 Citation

```bibtex
@article{rubab2025promptguard,
  title={Towards Detection and Mitigation of Distributed Prompt Jailbreak Attacks on Large Language Models},
  author={Warshia Rubab },
  journal={IEEE Research Paper},
  year={2026},
  institution={National University of Technology (NUTECH), Islamabad}
}
```

---

# 👥 Author & Contact

| Name | Role | Contact |
|------|------|---------|
| **Warshia Rubab** | Lead Researcher | [warshiarubab9427@gmail.com](mailto:warshiarubab9427@gmail.com) |

### **Supervisor**: Sir Babar Yousaf · NUTECH Islamabad

---

# 📧 Connect with Me

- **Email**: [warshiarubab9427@gmail.com](mailto:warshiarubab9427@gmail.com)
- **LinkedIn**: [linkedin.com/in/warshia-rubab-3191b039b](https://linkedin.com/in/warshia-rubab-3191b039b)

⭐ If you find this research useful, please consider giving it a star!




