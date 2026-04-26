# EuroHPC-TVB-Digital-Twin

> Personalized whole-brain simulation digital twins on EuroHPC infrastructure.
> A collaboration between **SNU Connectome Lab (Transconnectome I / Diver)** and **Viktor Jirsa's TVB group (EBRAINS / INS, Aix-Marseille University)**.

---

## 🧠 What Is This Project?

We are building **personalized brain digital twins** — subject-specific computational models that simulate whole-brain dynamics using [The Virtual Brain (TVB)](https://www.thevirtualbrain.org/) platform. Our goal is to scale these simulations from single subjects to **population-level (1,000+ subjects)** using EuroHPC supercomputers.

### Why It Matters
- **Precision Psychiatry**: Virtual brain twins enable patient-specific predictions for psychiatric disorders (OCD, schizophrenia, depression).
- **Connectome-Informed**: Models are parameterized by individual structural connectivity from diffusion MRI.
- **Scalable Inference**: Bayesian parameter estimation across thousands of subjects requires massive GPU resources unavailable at institutional scale.

---

## 🤝 Key Collaborators

### Viktor Jirsa (Aix-Marseille / EBRAINS)
- **Chief Science Officer** of EBRAINS AISBL
- **Director** of Inserm Institut de Neurosciences des Systèmes (INS)
- Co-creator of The Virtual Brain (TVB)
- Leads **Virtual Brain Twin Project** (2024–2027, €10M EU Horizon Health grant) — virtual brain twins for psychiatric disorders
- Leads **EBRAINS 2.0 WP3**: "Creating Digital Twins through Modelling and Simulation"
- Key publications:
  - "Principles and Operation of Virtual Brain Twins" (Apr 2024)
  - "Virtual brain twins for stimulation in epilepsy" (Apr 2025)
  - "Virtual Brain Inference (VBI)" toolkit (Jul 2025)

### SNU Connectome Lab (Cha Ji-wook)
- **Transconnectome I — Diver Project**: Connectome-based deep learning for brain disorder classification
- Expertise in fMRI/dMRI analysis, contrastive learning, brain network modeling
- Current infrastructure: DGX Spark (local GPU cluster)

### Collaboration Goal
Combine Jirsa's TVB framework with our connectome-based deep learning (Diver) to create a **hybrid simulation-ML pipeline** for personalized brain digital twins at EuroHPC scale.

→ See [Collaboration Plan](docs/jirsa_collaboration_plan.md) for details.

---

## 📅 Timeline & Milestones

| Date | Milestone | Status |
| :--- | :--- | :--- |
| **2026 May** | Benchmark Access 신청 (monthly rolling) | `Next` |
| **2026 May–Jul** | Scaling tests on LUMI/Leonardo (3개월) | `Planned` |
| **2026 Sep 4** | Regular Access 마감 (10:00 CEST) | `Target` |
| **2027 Jan** | Regular Access 결과 발표 | — |
| **2027 Jan–Jan 2028** | Production runs (1M+ GPU-hours) | — |
| **2027 H1** | Joint publication with Jirsa group | — |

### EuroHPC 2026 주요 마감일 (참고)

| Access Mode | Cut-off | 결과 발표 |
| :--- | :--- | :--- |
| Benchmark | 매월 1일 (rolling) | 제출 후 2–3주 |
| Development | 매월 1일 (rolling) | 제출 후 2–3주 |
| Regular | **2026-09-04** | 2027-01 |
| Extreme Scale | 2026-10-19 | 2027-03 |

---

## 📊 EuroHPC Access Strategy

```
Phase 1: Benchmark Access (2026 Q2)
  └─ TVB scalability test, GPU utilization profiling
  └─ Target: LUMI-G or Leonardo (GPU partitions)
  └─ Duration: 3 months, limited node-hours

Phase 2: Regular Access — Scientific Track (2026 Q3 submission)
  └─ 1,000,000 GPU-hours for population-scale simulation
  └─ Benchmark results as evidence of scalability
  └─ 12-month allocation period

Phase 3 (Future): Extreme Scale Access
  └─ Full-scale digital twin deployment
  └─ Requires Phase 2 track record
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
    ├── jirsa_collaboration_plan.md    # TVB group collaboration strategy
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

### TVB & EBRAINS
- [The Virtual Brain](https://www.thevirtualbrain.org/)
- [EBRAINS Platform](https://ebrains.eu/)
- [Virtual Brain Twin Project](https://ebrains.eu/impact/projects/virtual-brain-twin)

### Transconnectome / Diver
- [Transconnectome GitHub](https://github.com/Transconnectome)

---

## 🚀 Quick Start (Onboarding)

**신규 참여자를 위한 가이드:**

1. **배경 이해**: 이 README 전체를 읽고 프로젝트의 목표와 전략을 파악합니다.
2. **TVB 숙지**: [TVB documentation](https://docs.thevirtualbrain.org/)에서 기본 시뮬레이션 파이프라인을 이해합니다.
3. **Diver 프로젝트**: [docs/projects/diver/](docs/projects/diver/README.md)에서 커넥톰 기반 딥러닝 파이프라인을 확인합니다.
4. **EuroHPC 신청**: [docs/eurohpc_application.md](docs/eurohpc_application.md)에서 신청 절차와 요구사항을 확인합니다.
5. **벤치마크**: [benchmarks/scaling_plan.md](benchmarks/scaling_plan.md)에서 스케일링 테스트 설계를 확인합니다.
6. **GPU 시간 산정**: [proposal/gpu_hour_justification.md](proposal/gpu_hour_justification.md)에서 자원 요구량 근거를 확인합니다.

---

*Maintained by [SNU Connectome Lab](https://github.com/Transconnectome) — Seoul National University, Department of Psychology.*
