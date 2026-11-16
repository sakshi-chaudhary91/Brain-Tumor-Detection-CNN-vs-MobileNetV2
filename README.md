# 🧠 Brain Tumor Detection & Model Comparison (CNN vs MobileNetV2)

An end-to-end deep learning project for classifying brain MRI scans into four distinct categories using the Masoud Nickparvar Brain Tumor MRI Dataset. This project compares the performance of a **Custom Convolutional Neural Network (CNN) built from scratch** against a **Pre-trained MobileNetV2 Transfer Learning model**. 

---

## 📊 Dataset Overview
The dataset consists of MRI images categorized into **4 classes**: 
1. **Glioma Tumor**
2. **Meningioma Tumor**
3. **Pituitary Tumor**
4. **No Tumor**

* **Image Dimensions:** `150x150x3`
* **Data Splits:** Training, Validation, and Testing sets powered by Keras Image Data Generators.

---

## 🏗️ Model Architectures

### 1. Custom CNN (Scratch)
* **Architecture:** Sequential model comprising multiple Conv2D layers, Batch Normalization, Max Pooling, Dropout regularization, and Dense classification layers.
* **Result:** Achieved strong validation accuracy (~93.21%) and an unseen test accuracy of **84.44%**.

### 2. Transfer Learning (MobileNetV2)
* **Architecture:** MobileNetV2 pre-trained on ImageNet with frozen base weights, coupled with a custom classification head (`GlobalAveragePooling2D`, `Dense(512)`, `Dropout(0.5)`, and `Dense(4, softmax)`).
* **Result:** Reached a validation accuracy of **92.50%** and an unseen test accuracy of **82.13%** with a significantly lower test loss (`0.7523`), indicating high prediction confidence.

---

## 📈 Performance Summary

| Model | Validation Accuracy | Test Accuracy | Test Loss |
| :--- | :---: | :---: | :---: |
| **Custom CNN (Scratch)** | 93.21% | **84.44%** | 1.1915 |
| **MobileNetV2 (Frozen Base)** | 92.50% | 82.13% | **0.7523** |

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Deep Learning Framework:** TensorFlow / Keras
* **Data Handling & Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Kaggle Notebooks 

---
