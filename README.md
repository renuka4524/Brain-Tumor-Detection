# 🧠 Brain Tumor Detection using CNN

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=for-the-badge&logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-red?style=for-the-badge&logo=keras)
![Accuracy](https://img.shields.io/badge/Test%20Accuracy-88.7%25-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-Apache%202.0-blue?style=for-the-badge)

> A deep learning model that detects brain tumors from MRI scans using a Convolutional Neural Network (CNN) built with TensorFlow and Keras — achieving **88.7% accuracy** and **0.88 F1 score** on the test set.

---

## 📌 Project Overview

Brain tumor detection from MRI images is a critical medical imaging task. Manual diagnosis is time-consuming and prone to human error. This project automates the detection process using a CNN trained on labeled MRI scan data.

**Key Highlights:**
- Binary classification: Tumor (Yes) vs No Tumor (No)
- Trained on 253 Brain MRI images from Kaggle
- Applied **Data Augmentation** to handle small dataset size
- Best model selected based on validation accuracy

---

## 📊 Results

| Metric | Validation Set | Test Set |
|--------|---------------|----------|
| Accuracy | 91% | 88.7% |
| F1 Score | 0.91 | 0.88 |

---

## 🗂️ Dataset

- **Source:** [Kaggle Brain MRI Images](https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection)
- **Total Images:** 253
  - `yes/` — 155 tumorous MRI images
  - `no/` — 98 non-tumorous MRI images

---

## 🏗️ Model Architecture

```
Input (MRI Image)
      ↓
Conv2D + ReLU
      ↓
MaxPooling2D
      ↓
Conv2D + ReLU
      ↓
MaxPooling2D
      ↓
Flatten
      ↓
Dense (Fully Connected)
      ↓
Output (Sigmoid → Yes/No)
```

---

## 🔄 Data Augmentation

Since the dataset only has 253 images, data augmentation was applied to:
- Prevent overfitting
- Artificially increase training data variety

Techniques: Rotation, Width/Height shift, Horizontal flip, Zoom

---

## 🚀 Getting Started

```bash
pip install tensorflow keras numpy matplotlib scikit-learn opencv-python
git clone https://github.com/renuka4524/Brain-Tumor-Detection.git
cd Brain-Tumor-Detection
jupyter notebook "Brain Tumor Detection.ipynb"
```

---

## 💾 Loading the Best Model

```python
from tensorflow.keras.models import load_model
best_model = load_model(filepath='models/cnn-parameters-improvement-23-0.91.model')
```

---

## 🛠️ Tech Stack

- **Language:** Python 3.8+
- **Deep Learning:** TensorFlow, Keras
- **Data Processing:** NumPy, OpenCV, PIL
- **Visualization:** Matplotlib
- **Evaluation:** Scikit-learn

---

## 🙋 Author

**Renuka** — BTech CSE  
📧 [renukam2611@gmail.com]  
🔗 [www.linkedin.com/in/renuka-madhasani]  
🐙 [github.com/renuka4524](https://github.com/renuka4524)

---

## 📄 License

Apache 2.0 — see [LICENSE](LICENSE) for details.

---

⭐ *If you found this project useful, consider giving it a star!*
