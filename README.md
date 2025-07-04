# Efficacy Check of Haralick and Symmetry Features for Skin Lesions Classification

This project evaluates the effectiveness of Haralick texture features and symmetry-based features in classifying skin lesion images (e.g., benign vs malignant). 
Paper Link:
https://www.ijcaonline.org/archives/volume185/number3/laud-2023-ijca-922679.pdf
---

## 📌 Table of Contents
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Features](#features)
- [Methodology](#methodology)

---

## 🩺 Introduction
Skin cancer diagnosis can benefit from automated image-based classification. This project tests the efficacy of:
- Haralick texture features (from gray-level co-occurrence matrices)
- Symmetry-based features (image asymmetry across axes)

We evaluate their utility using traditional machine learning classifiers on a skin lesion dataset.

---

## 🎯 Objectives
- Extract Haralick and symmetry features from lesion images.
- Train ML classifiers (e.g., SVM, KNN) on these features.
- Compare classification performance:
  - Haralick-only
  - Symmetry-only
  - Combined
  - (Optional) Deep learning baseline

---

## 📂 Dataset
- Source: [ISIC Archive / ISIC 2018 Challenge](https://challenge.isic-archive.com/)
- Task: Binary classification (benign vs malignant)
- Preprocessing:
  - Resizing
  - Grayscale conversion
  - Optional segmentation/masking

---

## 🧩 Features
### Haralick Features
- Extracted via Gray-Level Co-Occurrence Matrix (GLCM)
- Properties:
  - Contrast
  - Correlation
  - Energy
  - Homogeneity
  - Etc.

### Symmetry Features
- Quantify asymmetry along vertical and horizontal axes
- Computed as pixel-wise differences between mirrored halves

---

## ⚙️ Methodology
1. **Data Preparation**
   - Download and preprocess images.
   - Label: Benign / Malignant.
2. **Feature Extraction**
   - Haralick features via scikit-image.
   - Symmetry measures via custom code.
3. **Feature Fusion**
   - Combine feature vectors.
4. **Modeling**
   - Train/test splits or cross-validation.
   - Classifiers: SVM, KNN, Random Forest.
5. **Evaluation**
   - Accuracy, Precision, Recall, F1-score, ROC-AUC.
6. **Comparison**
   - Haralick-only
   - Symmetry-only
   - Combined
   - Optional CNN embeddings baseline.
