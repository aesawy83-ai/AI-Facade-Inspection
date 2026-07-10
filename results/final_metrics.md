## 📊 Results Summary

The current baseline **YOLO11 multi-class façade defect detector** demonstrates measurable learning across all four target defect classes, with the strongest performance on **crack detection** and the weakest performance on **thin-object wire detection**.

# Final Model Metrics

## Model Configuration

- Model: YOLO11s
- Dataset: FMP Combined Dataset Version 1
- Classes: Crack, Spalling, Wire
- Epochs: 100
- Image size: 640
- Batch size: 16
- GPU: NVIDIA Tesla T4

## Validation Results

| Metric | Value |
|---|---:|
| Precision | 0.916 |
| Recall | 0.828 |
| mAP@0.5 | 0.882 |
| mAP@0.5:0.95 | 0.781 |

## Class-wise AP@0.5:0.95

| Class | AP |
|---|---:|
| Crack | 0.684 |
| Spalling | 0.705 |
| Wire | 0.953 |

## Test Results

| Metric | Value |
|---|---:|
| Precision | 0.911 |
| Recall | 0.811 |
| mAP@0.5 | 0.890 |
| mAP@0.5:0.95 | 0.798 |

The latest model demonstrates a substantial improvement over the earlier
Three-class baseline. Wire detection achieved the strongest performance,
followed by spalling and crack detection.

### Performance Interpretation
The current model demonstrates the strongest feature learning for **cracks**, benefiting from clearer linear morphology and stronger representation in the dataset.  
The **wires class remains the weakest**, primarily due to:
- thin-object sensitivity
- scale variation
- background clutter
- limited hard negative examples
- lower class balance in the current dataset version

These findings directly inform the next dataset balancing and augmentation strategy for future iterations.
