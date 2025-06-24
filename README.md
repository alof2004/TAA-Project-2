# Automated Diagnosis of Alzheimer’s Disease Using Medical Imaging

This project was developed as part of the **Machine Learning Topics 2024/2025** course at the **University of Aveiro**. It explores the automated classification of Alzheimer’s disease using **MRI scans**, combining **radiomic feature extraction** and **deep learning** techniques.

## Project Overview

Alzheimer’s disease is the leading cause of dementia globally, and early detection is critical for patient care. This project investigates various machine learning and deep learning models to classify cognitive impairment levels based on brain MRI data.

### Objectives

- Classify MRI brain scans into four levels of impairment:  
  `No Impairment`, `Very Mild`, `Mild`, and `Moderate Impairment`.
- Compare traditional ML models (XGBoost, SVM) with CNN-based architectures (VGG16, ResNet50, EfficientNetB0).
- Address class imbalance and real-world applicability through binary classification reformulation and hybrid model strategies.

## Dataset

- Source: [Kaggle Alzheimer’s MRI Dataset](https://www.kaggle.com/datasets/lukechugh/best-alzheimer-mri-dataset-99-accuracy)
- 11,519 grayscale MRI images labeled across 4 impairment levels.
- Balanced training/validation sets; imbalanced test set to simulate clinical conditions.

## Methodology

### Traditional Machine Learning
- **Radiomic feature extraction** (texture, shape, frequency, entropy, asymmetry).
- Models: **XGBoost** and **Support Vector Machines (SVM)**.
- Binary and multiclass classification.
- Results:  
  - XGBoost (binary): 86.8% accuracy  
  - SVM (binary): 87.9% accuracy  

### Deep Learning
- Architectures: **VGG16**, **ResNet50**, and **EfficientNetB0**
- Transfer learning with fine-tuning in three stages.
- Techniques: early stopping, data augmentation, test-time augmentation.
- Best results:
  - **EfficientNetB0** achieved **96.56%** test accuracy with strong generalization and low sensitivity to class imbalance.

## Key Findings

- Lightweight models like EfficientNetB0 can outperform larger networks (ResNet50) on imbalanced medical datasets.
- Traditional models (SVM, XGBoost) remain competitive and interpretable, especially useful in hybrid pipelines.
- Binary reformulation improves sensitivity in early-stage impairment detection.

## Technologies Used

- Python
- Scikit-learn
- TensorFlow / Keras
- XGBoost
- OpenCV
- Matplotlib, Seaborn

## Authors

- **Afonso Ferreira** – NMEC 113480  
- **Tomás Brás** – NMEC 112665

## For more information on this project you can read our report which can be found here: [Report](https://github.com/alof2004/TAA-Project-2/blob/main/report_taa.pdf)

## Grade - 19.9
