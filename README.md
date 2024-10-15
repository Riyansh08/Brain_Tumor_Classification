# Brain Tumor Classification Project

This project implements **brain tumor classification** using **Custom CNN** and **Transfer Learning models**. It aims to classify MRI scans into **Meningioma, Glioma, Pituitary Tumors,** and **No Tumor** categories.

## Overview

### Project Objective:
- Build and compare two models:
  1. **Custom CNN Model:** A convolutional neural network trained from scratch.
  2. **Transfer Learning Model:** Fine-tuned ResNet50 pre-trained on ImageNet.
- Evaluate both models on the test dataset for **accuracy** and **confidence scores**.
- Use **Gradio** to deploy an interactive user interface.

---

## Dataset

The **Brain MRI Dataset** used in this project can be found on **Kaggle**:  
[Brain MRI Dataset](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)

- **Classes:**
  - Meningioma
  - Glioma
  - Pituitary Tumor
  - No Tumor

- **Preprocessing:**
  - Resize images to **128x128** pixels.
  - Normalize pixel values to the range [0, 1].
  - Convert to **grayscale** for the Custom CNN model.
  - Retain **RGB channels** for the Transfer Learning model.

---

## Project Structure

```plaintext
brain-tumor-classification/
│
├── models/
│   ├── custom_cnn_model.keras  # Custom CNN model
│   ├── transfer_model_v2.keras # Transfer Learning model
│
├── app.py                      # Gradio UI code
├── utils.py                    # Helper functions (preprocessing, predictions)
├── README.md                   # Project documentation (this file)
│
├── data/                       # Dataset directory
│   ├── train/
│   ├── val/
│   ├── test/
│
└── requirements.txt            # Dependencies
Future Improvements

Explainable AI Integration:
Use Grad-CAM to visualize regions influencing predictions.
Data Augmentation:
Add real-time augmentations to improve model robustness.
Enhanced Deployment:
Use Streamlit or Gradio to build more interactive UIs.
Multi-Label Classification:
Handle overlapping tumor conditions.
Conclusion

This project demonstrates the power of custom CNNs and transfer learning for brain tumor classification. While the results are promising, future improvements are needed to address misclassifications and enhance interpretability.
