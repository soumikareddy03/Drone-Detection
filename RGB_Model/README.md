# RGB Drone Detection Model

## Overview

This model performs drone detection using RGB imagery and YOLOv11n.

## Datasets

### Training and Validation

- IIT_DO_v1
- IIT_DO_v7
- DUT Dataset

### Dataset Statistics

| Dataset | Images | Train | Validation |
|----------|----------|----------|----------|
| IIT_DO_v1 | 3517 | 2813 | 704 |
| IIT_DO_v7 | 14490 | 11590 | 2898 |
| DUT | 5221 | 4605 | 616 |

### Testing

- Day Images
- Normal Images
- Thermal Split Images
- DUT Test Images

### Split Ratio

70 : 20 : 10

---

## Hyperparameters

| Parameter | Value |
|------------|--------|
| Model | YOLOv11n |
| Epochs | 30 |
| Image Size | 1024 |
| Batch Size | 16 |
| Mosaic | 1.0 |
| Scale | 0.5 |
| MixUp | 0.2 |

---

## Performance

| Metric | Value |
|----------|----------|
| Precision | 0.96 |
| Recall | 0.89 |
| mAP@50 | 0.917 |
| mAP@50-95 | 0.822 |
