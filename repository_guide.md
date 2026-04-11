#  Repository Guide

This document explains the **information architecture, folder responsibilities, artifact flow, and reviewer navigation path** of the **AI-Facade-Inspection** repository.

The repository is structured to support:
- **technical reproducibility**
- **research documentation**
- **benchmark traceability**
- **AECO workflow integration**
- **future BIM and Digital Twin extensions**

---
## Navigation Hub
This hub provides quick access to both the **technical repository workflow** and the **research methodology documentation system**.

|  Technical Repository Navigation |  Research Documentation Hub |
|---|---|
| [ Project Objective](#-project-objective) | [ Documentation Overview](docs/README.md) |
| [ Dataset and Defect Taxonomy](#-dataset) | [ Problem Framing and Context](docs/problem_framing.md) |
| [ Model Architecture and Training Setup](#️-model-architecture) | [ Research Question and Evaluation Lens](docs/research_question.md) |
| [ Results Summary and Benchmark KPIs](#-results-summary) | [ Class Definitions and Annotation Logic](docs/class_definitions.md) |
| [ Evaluation Curves and Visual Evidence](#-evaluation-visual-evidence) | [ Dataset Strategy and Growth Plan](docs/dataset_strategy.md) |
| [ Error Analysis and Failure Modes](#-error-analysis) | [ Future BIM and Digital Twin Integration](docs/future_integration.md) |
| [ Repository Structure and Artifacts](#-repository-structure) | [ Governance and Validation Checklist](docs/governance_checklist.md) |

---

## 📁 Root Repository Structure

```text
AI-Facade-Inspection/
│
├── README.md
├── requirements.txt
│
├── assets/
│   ├── facade_banner_v2.png
│   └── banner_01.png
│
├── notebooks/
│   └── FMP_AI_Facade_Inspection.ipynb
│
├── docs/
│   ├── README.md
│   ├── class_definitions.md
│   ├── collaborative_workflow.md
│   ├── dataset_strategy.md
│   ├── error_analysis.md
│   ├── future_integration.md
│   ├── governance_checklist.md
│   ├── problem_framing.md
│   ├── repository_guide.md
│   └── research_question.md
│
├── results/
│   ├── curves/
│   ├── evidence/
│   ├── predictions_new/
│   ├── predictions_val/
│   └── final_metrics.md
