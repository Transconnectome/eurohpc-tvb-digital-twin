# EuroHPC Digital Twin: Electrophysiology Foundation Model & AI Scientist

> **Core Vision**: Build an **Electrophysiology Foundation Model** and deploy **AI Scientist agents** for autonomous neuroscience discovery — powered by EuroHPC exascale infrastructure.
>
> A collaboration between **SNU Connectome Lab (Transconnectome I / Diver)** and **Viktor Jirsa's group (EBRAINS / INS, Aix-Marseille University)**.

---

## 🧠 Project Overview

### The Problem
Electrophysiology data (EEG, MEG, intracranial recordings) is massive, heterogeneous, and underutilized. Current analysis pipelines are task-specific, require extensive manual tuning, and don't generalize across datasets, devices, or populations.

### Our Solution: Two Pillars

#### Pillar 1 — Electrophysiology Foundation Model
A large-scale pretrained model that learns **universal neural representations** from diverse electrophysiology data:
- **Data**: Multi-modal (EEG, MEG, ECoG), multi-site, multi-device recordings — thousands of hours
- **Architecture**: Transformer-based with spatiotemporal tokenization (cf. BrainOmni, LaBraM, MEG-GPT)
- **Pretraining**: Self-supervised learning on raw neural signals — requires massive GPU compute
- **Downstream**: Zero-shot/few-shot transfer to disorder classification, BCI, cognitive decoding, biomarker discovery

#### Pillar 2 — AI Scientist for Neuroscience
Autonomous research agents (inspired by Sakana AI's AI Scientist) that:
- **Generate hypotheses** from literature and data patterns
- **Design and run experiments** on the foundation model
- **Analyze results**, produce figures, write manuscripts
- **Iterate** through tree-search-based exploration of the hypothesis space
- **Scale** with EuroHPC compute to explore thousands of experimental configurations in parallel

### Why EuroHPC?
- Foundation model pretraining on 1,000+ hours of neural data requires **sustained GPU-months**
- AI Scientist agents running parallel experiment trees multiply compute needs **10–100×**
- Institutional clusters (even DGX Spark) are insufficient for population-scale pretraining + autonomous exploration

---

## 🤝 Key Collaborators

### Viktor Jirsa (Aix-Marseille / EBRAINS)
- **Chief Science Officer**, EBRAINS AISBL
- **Director**, Inserm Institut de Neurosciences des Systèmes (INS)
- Co-creator of The Virtual Brain (TVB)
- Leads **Virtual Brain Twin Project** (2024–2027, €10M EU Horizon Health)
- Leads **EBRAINS 2.0 WP3**: Digital Twins through Modelling and Simulation
- **Role in this project**: Electrophysiology data access (EBRAINS datasets), simulation framework integration, clinical validation pipeline

### SNU Connectome Lab (Cha Ji-wook)
- **Transconnectome I — Diver Project**: Connectome-based deep learning for brain disorders
- Expertise: fMRI/dMRI/EEG analysis, contrastive learning, brain network modeling
- Infrastructure: DGX Spark (local development), EuroHPC (target production)
- **Role in this project**: Foundation model architecture, AI Scientist pipeline, training infrastructure

---

## 📅 Timeline & Milestones

| Date | Milestone | Status |
| :--- | :--- | :--- |
| **2026 May** | Benchmark Access 신청 (monthly rolling) | `Next` |
| **2026 May–Jul** | Foundation model scaling tests on LUMI/Leonardo | `Planned` |
| **2026 Jun** | AI Scientist prototype (local DGX Spark) | `Planned` |
| **2026 Sep 4** | **Regular Access 마감** (10:00 CEST) | `Target` |
| **2027 Jan** | Regular Access 결과 발표 | — |
| **2027 Jan–Dec** | Production: Foundation model pretraining (1M+ GPU-hours) | — |
| **2027 H1** | AI Scientist autonomous experiment runs | — |
| **2027 H2** | Joint publication with Jirsa group | — |

### EuroHPC 2026 주요 마감일

| Access Mode | Cut-off | 결과 발표 | 기간 |
| :--- | :--- | :--- | :--- |
| Benchmark | 매월 1일 (rolling) | 제출 후 2–3주 | 3개월 |
| Development | 매월 1일 (rolling) | 제출 후 2–3주 | — |
| **Regular** | **2026-09-04** | 2027-01 | **12개월** |
| Extreme Scale | 2026-10-19 | 2027-03 | 12개월 |

---

## 📊 EuroHPC Access Strategy

```
Phase 1: Benchmark Access (2026 Q2)
  ├─ Foundation model: single-node → multi-node scaling test
  ├─ AI Scientist: agent loop profiling, GPU utilization
  └─ Target system: LUMI-G or Leonardo (GPU partitions)

Phase 2: Regular Access — Scientific Track (2026 Sep submission)
  ├─ 1,000,000 GPU-hours for full pretraining + experiment runs
  ├─ Benchmark results as scalability evidence
  └─ 12-month allocation

Phase 3 (Future): Extreme Scale Access
  ├─ Population-scale foundation model (10K+ subjects)
  └─ Continuous AI Scientist operation
```

→ See [GPU Hour Justification](proposal/gpu_hour_justification.md) for compute breakdown.

---

## 📂 Repository Structure

```
eurohpc-tvb-digital-twin/
├── README.md                          # ← You are here
├── proposal/
│   └── gpu_hour_justification.md      # Compute resource breakdown (1M GPUh)
├── benchmarks/
│   └── scaling_plan.md                # Strong/weak scaling test design
├── gpu_hour_model/                    # Resource estimation models
├── scripts/                           # Automation & data collection
└── docs/
    ├── eurohpc_application.md         # Application guidelines & templates
    ├── jirsa_collaboration_plan.md    # Jirsa/EBRAINS collaboration strategy
    └── projects/
        └── diver/README.md            # Diver project integration
```

---

## 🔗 Resources

### EuroHPC
- [Access Portal (Apply Now)](https://access.eurohpc-ju.europa.eu/)
- [Access Policy & FAQ](https://eurohpc-ju.europa.eu/supercomputers/supercomputers-access-policy-and-faq_en)
- [Regular Access Call](https://www.eurohpc-ju.europa.eu/eurohpc-ju-call-proposals-regular-access-mode_en)
- [Benchmark Access Call](https://www.eurohpc-ju.europa.eu/eurohpc-ju-call-proposals-benchmark-access_en)

### Electrophysiology Foundation Models (State of the Art)
- [BrainOmni](https://arxiv.org/abs/2505.18185) — Unified EEG+MEG foundation model
- [LaBraM](https://openreview.net/forum?id=QzTpTRVtrP) — Large Brain Model (2,500h EEG pretraining)
- [MEG-GPT](https://arxiv.org/abs/2510.18080) — Transformer-based MEG foundation model

### AI Scientist
- [Sakana AI — The AI Scientist](https://sakana.ai/ai-scientist/)
- [AI Scientist v2](https://pub.sakana.ai/ai-scientist-v2/paper/paper.pdf) — Agentic tree-search for autonomous research

### EBRAINS & TVB
- [EBRAINS Platform](https://ebrains.eu/)
- [The Virtual Brain](https://www.thevirtualbrain.org/)
- [Virtual Brain Twin Project](https://ebrains.eu/impact/projects/virtual-brain-twin)

### Transconnectome / Diver
- [Transconnectome GitHub](https://github.com/Transconnectome)

---

## 🚀 Onboarding Guide

**신규 참여자를 위한 단계별 가이드:**

1. **이 README를 읽고** 프로젝트의 두 핵심 축(Foundation Model + AI Scientist)을 이해합니다.
2. **관련 논문 리뷰**: 위 Resources의 BrainOmni, LaBraM, AI Scientist v2 논문을 읽습니다.
3. **Diver 프로젝트 파악**: [docs/projects/diver/](docs/projects/diver/README.md)에서 커넥톰 기반 파이프라인을 확인합니다.
4. **Jirsa 협업 계획**: [docs/jirsa_collaboration_plan.md](docs/jirsa_collaboration_plan.md)에서 EBRAINS 연계 전략을 확인합니다.
5. **EuroHPC 신청 절차**: [docs/eurohpc_application.md](docs/eurohpc_application.md)에서 요구사항을 확인합니다.
6. **벤치마크 설계**: [benchmarks/scaling_plan.md](benchmarks/scaling_plan.md)에서 스케일링 테스트를 확인합니다.
7. **GPU 시간 산정**: [proposal/gpu_hour_justification.md](proposal/gpu_hour_justification.md)에서 자원 요구량을 확인합니다.

---

*Maintained by [SNU Connectome Lab](https://github.com/Transconnectome) — Seoul National University, Department of Psychology.*
