# Future Integration Roadmap

The current repository implements the façade crack detection stage only.

## Planned Next Steps

### 1. Structure
Convert detections into structured outputs such as:
- defect class
- confidence
- pixel area
- severity category
- evidence image reference

### 2. Integrate
Associate structured defect outputs with BIM / IFC / Revit elements using future model-mapping logic.

### 3. Assess
Support persistent condition records and maintenance-oriented decision workflows.

## Example Future Output Schema
```json
{
  "asset_id": "WALL_N_04",
  "defect_type": "crack",
  "confidence": 0.98,
  "severity": "high",
  "pixel_area": 450
}

This follows the structured output and BIM-association concepts in the PDF. :contentReference[oaicite:8]{index=8}

---

## Step 10 — Create `docs/collaborative_workflow.md`
**Tool:** GitHub → `docs/` → create new file

Filename:
```text
docs/collaborative_workflow.md
# Collaborative Workflow

This project is part of a multidisciplinary Final Masters Project (FMP) focused on AI-enabled façade inspection and digital twin integration.

## Team Collaboration Logic
The broader project combines:
- Computer Vision
- BIM Integration
- Statistical Validation
- AECO Domain Knowledge

## Current Repository Role
This repository primarily supports the Computer Vision stream by providing:
- defect detection experiments
- training notebooks
- evaluation outputs
- evidence for reproducibility

Future integration will connect this work with BIM association, structured outputs, and decision-support workflows.
