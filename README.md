# Smart Parking: Parking Space Detection Using Computer Vision

This repository contains the code, model results, and analysis for the project **"Smart Parking: Parking Space Detection Using Computer Vision"**, which explores multiple deep learning models to classify parking slots as **empty** or **occupied** using the PKLot-v2 640 dataset.

---

## Models Implemented

1. **CNN from Scratch (TensorFlow)**
2. **ResNet50 + Custom Classifier (TensorFlow)**
3. **ResNet50 Fine-tuned (PyTorch)**
4. **Vision Transformer (ViT)**

---

## Evaluation Summary

| Model | F1 Score (Best) | AUC-ROC | Threshold |
|-------|------------------|----------|-----------|
| CNN Scratch | 0.93 | 0.9438 | 0.32 |
| ResNet50 TF | 0.96 | 0.9695 | 0.55 |
| ResNet50 PT | 1.00 | 0.9999 | 0.03 |
| ViT          | 1.00 | 0.9998 | 0.57 |

> ✔ ViT was selected for final deployment via Gradio demo.

---

## Validation & Test Metric Highlights

- ViT and ResNet50 (PyTorch) achieved perfect F1, Precision, Recall on both validation and test sets.
- TensorFlow ResNet50 showed strong generalization and consistent results.
- Custom CNN had high recall but lower precision on test data.

---

## Limitations

- Dataset is limited to fixed parking layouts from Brazil
- Static images only; not evaluated on video or real-time data
- Parking slot localization was not part of the pipeline
- No environmental diversity (night, snow, etc.)
- No latency testing for real-time edge deployment

---

## Future Enhancements

- Integrate YOLO/SSD for real-time slot detection
- Train with weather and lighting variations
- Deploy on Raspberry Pi or Jetson Nano
- Build mobile app to guide drivers
- Use Grad-CAM/attention maps for explainability
- Set up model monitoring and retraining pipeline

---

## Author's Note

This project was developed to explore the practical application of CNNs and transformers in visual classification tasks. It offered hands-on exposure to model training, evaluation, visualization, and deployment, and served as a valuable learning experience in building intelligent, real-world AI systems.

---

## Resources

- PKLot Dataset (via Roboflow)
- TensorFlow, PyTorch, Hugging Face Transformers
- Gradio for app UI
- Matplotlib, Seaborn for metric visualization

