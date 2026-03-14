# Error Analysis

## Overview
The crack detection model achieved mAP@0.5 = 0.825. While performance is strong overall, failure cases remain in challenging visual conditions.

---

## False Positives (FP)

1. High-contrast facade lines incorrectly classified as cracks.
2. Surface shadows detected as structural damage.
3. Texture discontinuities mistaken for fine cracks.

---

## False Negatives (FN)

1. Very thin hairline cracks missed at 640 resolution.
2. Low-contrast cracks on bright surfaces undetected.
3. Partially occluded crack regions not fully localized.

---

## Improvement Plan

1. Increase dataset size with more thin crack examples.
2. Increase input resolution (imgsz=768).
3. Add brightness/contrast augmentation.
4. Train longer (50 epochs).

---

## Risk Note

False negatives are more critical than false positives in structural inspection.  
Human validation is recommended.
