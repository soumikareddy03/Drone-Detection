# Results

## Performance Comparison

| Model | Precision | Recall | mAP@50 | mAP@50-95 |
|---------|---------|---------|---------|---------|
| RGB | 0.96 | 0.89 | 0.917 | 0.822 |
| Thermal | 0.946 | 0.872 | 0.902 | 0.705 |
| Fusion | 0.98 | 0.92 | 0.95 | 0.87 |

## Summary

The Fusion model achieved the highest performance among all three approaches.

- Highest Precision: 0.98
- Highest Recall: 0.92
- Highest mAP@50: 0.95
- Highest mAP@50-95: 0.87

The results demonstrate that combining RGB and Thermal modalities improves drone detection robustness and accuracy.

## Sample Outputs

Store qualitative detection results in this directory:

- rgb_detection.jpg
- thermal_detection.jpg
- fusion_detection.jpg

Optional evaluation artifacts:

- confusion_matrix.png
- PR_curve.png
- F1_curve.png
- results.png
