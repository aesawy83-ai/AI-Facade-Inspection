#  Repository Guide

This document explains the **information architecture, folder responsibilities, artifact flow, and reviewer navigation path** of the **AI-Facade-Inspection** repository.

The repository is structured to support:

* technical reproducibility
* research documentation
* benchmark traceability
* AECO workflow integration
* BIM and Digital Twin system design

---

##  Navigation Hub

This hub provides quick access to both the **technical repository workflow** and the **research methodology documentation system**.

| Technical Repository Navigation                                       | Research Documentation Hub                                               |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [Project Objective](#-project-objective)                              | [Documentation Overview](docs/README.md)                                 |
| [Dataset and Defect Taxonomy](#-dataset)                              | [Problem Framing and Context](docs/problem_framing.md)                   |
| [Model Architecture and Training Setup](#️-model-architecture)        | [Research Question and Evaluation Lens](docs/research_question.md)       |
| [Results Summary and Benchmark KPIs](#-results-summary)               | [Class Definitions and Annotation Logic](docs/class_definitions.md)      |
| [Evaluation Curves and Visual Evidence](#-evaluation-visual-evidence) | [Dataset Strategy and Growth Plan](docs/dataset_strategy.md)             |
| [Error Analysis and Failure Modes](#-error-analysis)                  | [Future BIM and Digital Twin Integration](docs/future_integration.md)    |
| [Repository Structure and Artifacts](#-repository-structure)          | [Governance and Validation Checklist](docs/governance_checklist.md)      |
|                                                                       | [🧠 Digital Twin Integration Strategy](docs/digital_twin_integration.md) |

---

##  System Overview

The repository implements an **AI-enabled façade inspection system** that extends from computer vision detection to **BIM-integrated Digital Twin workflows**.

```text
Capture → Detect → Structure → Integrate → Assess
```

Implemented as:

```text
Image → YOLO Detection → Structured JSON → BIM / IFC → Digital Twin → Dashboard
```

This ensures the repository functions as a **complete inspection intelligence system**, not just a model implementation.

---

##  Root Repository Structure

```text
AI-Facade-Inspection/
│
├── README.md
├── requirements.txt
│
├── assets/
│   ├── facade_banner_v2.png
│   ├── banner_01.png
│   ├── pipeline_dt_v2.png
│   ├── bim_logic_v2.png
│   └── dt_lifecycle_v2.png
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
│   ├── research_question.md
│   └── digital_twin_integration.md
│
├── results/
│   ├── curves/
│   ├── evidence/
│   ├── predictions_new/
│   ├── predictions_val/
│   └── final_metrics.md
```

---

##  Artifact Flow

The repository follows a structured data and workflow progression:

```text
Inspection Images
        ↓
YOLO Detection (notebook)
        ↓
Structured Outputs (predictions + metrics)
        ↓
Results Folder (curves, evidence, predictions)
        ↓
Documentation (analysis, governance, integration)
        ↓
BIM + Digital Twin Conceptual Integration
```

---

##  Folder Responsibilities

### 🔹 assets/

Stores all **visual assets and system diagrams**, including:

* project banner
* pipeline diagram
* BIM association logic
* Digital Twin lifecycle visualization

---

### 🔹 notebooks/

Contains the **core experimentation and training workflow**:

* model training
* validation
* inference
* export of results

---

### 🔹 docs/

Represents the **research and system design layer** of the repository:

* problem framing and research logic
* dataset governance and annotation strategy
* benchmarking and validation
* BIM and Digital Twin integration
* lifecycle and workflow modeling

---

### 🔹 results/

Contains all **model outputs and evaluation artifacts**:

* training curves
* confusion matrix
* PR / F1 curves
* validation predictions
* unseen test evidence
* final performance metrics

---

##  Digital Twin Integration Layer

The repository includes a dedicated Digital Twin architecture:

 [`docs/digital_twin_integration.md`](docs/digital_twin_integration.md)

This layer defines how detection outputs are transformed into:

* structured defect records
* BIM-linked condition data
* time-based lifecycle tracking
* inspection intelligence workflows

It formalizes the system as a **state-based Digital Twin model**:

```text
T1 → Detection
T2 → Deterioration
T3 → Repair / Closure
```

---

##  Reviewer Navigation Path

For efficient evaluation, follow this order:

1. README.md → system overview and results
2. notebooks/ → training and experimentation
3. results/ → model outputs and performance
4. docs/ → methodology and system design
5. digital_twin_integration.md → full system architecture

---

##  Final Note

This repository is structured not only as a machine learning project, but as a **complete AI-enabled inspection system aligned with BIM and Digital Twin workflows**.

It demonstrates how computer vision outputs can be transformed into **structured, scalable, and lifecycle-aware asset intelligence**.
