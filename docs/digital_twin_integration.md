# 🧠 Digital Twin Integration Strategy

## 🎯 Purpose

This repository currently implements the **Detect** stage of the façade inspection workflow using YOLO-based multi-class defect detection.

The wider project vision extends this into a Digital Twin workflow where image-based detections are transformed into **structured, traceable, BIM-linked condition intelligence**.

---

## 🧭 Target Workflow

```text
Capture → Detect → Structure → Integrate → Assess
```

### 🔗 Technical Pipeline Mapping

The conceptual workflow maps to the implemented system pipeline as follows:

```text
Image → YOLO Detection → Structured JSON → BIM / IFC → Digital Twin → Dashboard
```

---

## 🏗️ Digital Twin Role

The Digital Twin layer is responsible for converting façade defect detections into **persistent asset condition records**.

It is not limited to visual detection. Its role is to support:

* BIM-linked defect records
* element-level condition tracking
* evidence-based maintenance prioritisation
* longitudinal façade health monitoring
* lifecycle asset intelligence

---

## 🔄 Data Flow

```text
Inspection Image
↓
YOLO Detection
↓
Structured Defect Record
↓
BIM / IFC Element Association
↓
Digital Twin Condition Update
↓
Dashboard / Maintenance Decision
```

---

## 🧾 Structured Defect Record

Each detection should be converted into a structured JSON/CSV record.

### Example

```json
{
  "defect_id": "DEF_0001",
  "asset_id": "WALL_N_04",
  "ifc_guid": null,
  "defect_type": "crack",
  "confidence": 0.98,
  "severity": "high",
  "bbox": [120, 85, 460, 220],
  "pixel_area": 450,
  "image_id": "IMG_0234",
  "evidence_link": "results/predictions_new/IMG_0234.jpg",
  "association_status": "pending_review"
}
```

---

## 🏢 BIM Association Logic

Defects should only be linked to BIM elements when spatial confidence is acceptable.

The system should avoid forced BIM association.

### Recommended Statuses

* `validated`
* `candidate`
* `pending_review`
* `withheld`

### Association Criteria

* camera pose quality
* image-to-model alignment
* nearest façade surface distance
* projected defect location
* manual reviewer confirmation

### 🔍 Decision Logic Mapping

The BIM association workflow follows a validation-first approach:

* Detection outputs are passed through spatial validation
* If confidence and spatial alignment are high → automatically linked to BIM element
* If confidence is low or ambiguous → flagged for manual review

---

## 🔗 Revit / IFC Integration

Future implementation may include:

* IFC GUID tagging
* Revit shared parameter updates
* Dynamo/Revit API integration
* external defect registers linked to BIM elements
* clickable evidence links from BIM to inspection images

### Suggested Revit Parameters

* Facade_Condition
* Defect_Count
* Dominant_Defect_Type
* Highest_Severity
* Last_Inspection_Date
* AI_Confidence
* Evidence_Link
* Review_Status

---

## 📈 Digital Twin Update Principle

The Digital Twin should be updated through **controlled records**, not uncontrolled model overwrites.

Each inspection creates a new condition state.

---

## 🧠 Condition State Model

The Digital Twin operates as a **state-based system** where each inspection updates the condition of an asset over time.

Each state represents a snapshot of the asset condition:

* T1 → Initial detection
* T2 → Condition deterioration or progression
* T3 → Maintenance action and closure

### Example

```text
T1 → Crack detected → Medium severity
T2 → Crack expanded → High severity
T3 → Repair completed → Closed
```

This enables:

* trend analysis
* maintenance planning
* lifecycle decision-making

---

## 🔗 Integrated System View

The three core components of the system operate together:

* The **AI Pipeline** transforms images into structured defect data
* The **BIM Association Logic** determines how defects are linked to physical building elements
* The **Digital Twin Timeline** tracks how asset conditions evolve over time

Together, these layers enable a complete inspection intelligence workflow from detection to lifecycle decision-making.

---

## ⚠️ Safety and Review Gates

This repository is not intended to make standalone structural safety decisions.

Digital Twin updates should be reviewed when:

* detection confidence is low
* image quality is poor
* BIM association is uncertain
* defect class is safety-critical
* severity is high
