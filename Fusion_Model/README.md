# RGB-Thermal Fusion Drone Detection Model

## Overview

This model performs drone detection using fused RGB and Thermal imagery.

Fusion was performed using weighted pixel-level fusion:

Fusion Image = (0.6 × RGB) + (0.4 × Thermal)

## Datasets

### Training and Validation

- IIT_DO_v2
- IIT_DO_v7
- DUT Dataset

### Dataset Statistics

| Dataset | Images | Train | Validation |
|----------|----------|----------|----------|
| IIT_DO_v2 | 2370 | 1896 | 474 |
| IIT_DO_v7 | 14490 | 11590 | 2898 |
| DUT (Fused) | 5221 | 4605 | 616 |

### Testing

- Day Images
- Normal Images
- Thermal Images
- Split Images
- DUT Test Images

Total Test Images:

1817 RGB + 4039 Thermal

### Split Ratio

75 : 15 : 10

---

## Hyperparameters

| Parameter | Value |
|------------|--------|
| Model | YOLOv8s |
| Epochs | 30 |
| Image Size | 1024 |
| Batch Size | 8 |
| Mosaic | 1.0 |
| Scale | 0.5 |
| MixUp | 0.2 |

---

## Performance

| Metric | Value |
|----------|----------|
| Precision | 0.98 |
| Recall | 0.92 |
| mAP@50 | 0.95 |
| mAP@50-95 | 0.87 |
