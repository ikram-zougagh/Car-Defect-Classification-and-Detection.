# 🚗 Project: Car Damage Classification and Defect Detection

![Car Classification](https://img.shields.io/badge/Project-Car_Classification-orange?style=for-the-badge&logo=car&logoColor=white)
![Detectron2](https://img.shields.io/badge/Framework-Detectron2-blue?style=for-the-badge&logo=python&logoColor=white)

## 🌟 Project Description
This project aims to classify cars into damaged and undamaged categories using two neural network models: **CNN** and **VGG19**. After classification, we utilized **Detectron2** for defect detection on a different dataset.

## 🎯 Objectives
- Compare the performance of **CNN** and **VGG19** for binary classification.
- Use **Detectron2** for defect detection on car images.

## 📊 Classification Models
We trained two different models for the binary classification of cars into damaged and undamaged categories. Here are the details:

### **CNN Model**
We built a custom Convolutional Neural Network (**CNN**) trained on a dataset of damaged and undamaged car images. The CNN achieved an impressive validation accuracy of **91.46%**. This model generalized well on unseen data, making it a solid choice for this classification task.

#### **CNN Results:**
- **Validation Accuracy**: 91.46%
- **Validation Loss**: Low loss, indicating good generalization.
- **Evaluation Metrics**: Precision, recall, and F1-score were calculated and showed good performance in classifying both classes.

### **VGG19 Model**
We also tested the **VGG19** model, a pre-trained architecture, to compare its performance with the CNN. VGG19 demonstrated slightly lower accuracy, with signs of overfitting indicated by notable fluctuations in validation results.

#### **VGG19 Results:**
- **Validation Accuracy**: 50%
- **Issues Encountered**: Observed overfitting, leading to lower performance compared to CNN.
- **Evaluation Metrics**: Precision, recall, and F1-score were significantly lower than those of CNN.

## ⚖️ Model Comparison
The **CNN** outperformed **VGG19** in terms of generalization and accuracy, making it the best model for the binary classification of damaged and undamaged cars in our case.

## 🔍 Defect Detection with Detectron2
After classification, we used **Detectron2**, an object detection framework developed by **Meta** (formerly Facebook AI), for detecting defects in cars. We employed a different dataset specifically designed for visual defect detection.

### **Steps:**
- **Data Preprocessing**: We prepared another dataset for detection with Detectron2.
- **Training**: We trained a detection model based on a **Faster R-CNN** architecture available in Detectron2.
- **Results**: The model effectively detected several types of visual defects in the test images.

## 📁 Datasets
- **Binary Classification**: A dataset containing images of damaged and undamaged cars was used to train the CNN and VGG19 models.
- **Defect Detection**: A second, distinct dataset was used for the detection task with Detectron2.

## 🏁 Conclusion
In conclusion, the analysis of results showed that **CNN** outperformed **VGG19** for binary classification of cars. Subsequently, **Detectron2** proved effective for defect detection, paving the way for integration into automatic defect detection systems for the automotive industry.

---


