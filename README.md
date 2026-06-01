# Multimodal Drone Detection using YOLO

## Project Overview

This project investigates drone detection using three different sensing modalities:

1. RGB Images
2. Thermal Images
3. RGB-Thermal Fusion Images

The objective is to improve drone detection performance under varying environmental conditions by leveraging complementary information from RGB and Thermal sensors.

---

## Methodology

Three independent object detection models were developed:

| Model | Input |
|---------|---------|
| RGB Model | RGB Images |
| Thermal Model | Thermal Images |
| Fusion Model | RGB + Thermal Images |

The Fusion model uses pixel-level fusion:

Fusion Image = (0.6 × RGB) + (0.4 × Thermal)

---

## Architecture

- YOLOv11n (RGB)
- YOLOv11n (Thermal)
- YOLOv8s (Fusion)

---

## Data Augmentation

The following augmentations were applied:

- Mosaic = 1.0
- MixUp = 0.2
- Scale = 0.5

---

## Performance Comparison

| Model | Precision | Recall | mAP@50 | mAP@50-95 |
|---------|---------|---------|---------|---------|
| RGB | 0.96 | 0.89 | 0.917 | 0.822 |
| Thermal | 0.946 | 0.872 | 0.902 | 0.705 |
| Fusion | 0.98 | 0.92 | 0.95 | 0.87 |

---

## Key Findings

- RGB images provide strong visual features.
- Thermal images improve robustness under poor illumination.
- Fusion combines complementary information from both modalities.
- Fusion achieved the highest detection accuracy across all evaluation metrics.

---

## Repository Structure

```text
Drone-Detection/
│
├── README.md
│
├── RGB_Model/
│   ├── README.md
│   └── rgb_training.ipynb
│
├── Thermal_Model/
│   ├── README.md
│   └── thermal_training.ipynb
│
├── Fusion_Model/
│   ├── README.md
│   └── fusion_training.ipynb
│
└── Results/
    ├── README.md
    ├── rgb_detection.jpg
    ├── thermal_detection.jpg
    ├── fusion_detection.jpg
