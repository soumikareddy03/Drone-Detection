# Thermal Drone Detection Model

## Overview

This model performs drone detection using Thermal imagery and YOLOv11n.

## Dataset

### Training and Validation

- DUT Dataset
- IIT Drone Thermal Split Images

### Dataset Statistics

| Dataset | Images |
|----------|----------|
| Train | 5600 |
| Validation | 1100 |
| Test | 1200 |

Each test video was converted into approximately 300 frames.

### Image Resolution

960 × 1080

### Split Ratio

70 : 15 : 15

---

## Hyperparameters

| Parameter | Value |
|------------|--------|
| Model | YOLOv11n |
| Epochs | 50 |
| Image Size | 640 |
| Batch Size | 16 |

---

## Performance

| Metric | Value |
|----------|----------|
| Precision | 0.946 |
| Recall | 0.872 |
| mAP@50 | 0.902 |
| mAP@50-95 | 0.705 |
