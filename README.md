# ECG Anomaly Detection on Edge Devices – TinyML & Machine Learning Approaches

This repository contains a self-made summary and recreation of the research paper: **["Reliable ECG Anomaly Detection on Edge Devices for Internet of Medical Things Applications"](https://www.mdpi.com/1424-8220/25/8/2496)**. The project focuses on **ECG anomaly detection** using the MIT-BIH Arrhythmia dataset, comparing classic machine learning models and deep learning (CNN), and exploring TinyML deployment concepts for edge devices.

---

## 🔹 Project Overview

Continuous ECG monitoring is essential for early detection of cardiac anomalies. This repository demonstrates two aspects:

1. **Machine Learning Models for ECG Classification**  
   - Decision Tree, Random Forest, XGBoost, and CNN  
   - Trained and evaluated on the MIT-BIH dataset  
   - Comparison of metrics (Accuracy, Precision, Recall, F1-Score) with reference results from the paper  

2. **Summary and insights from the original research paper**  
   - TinyML pipeline for deployment on edge devices (Arduino, Raspberry Pi)  
   - Model optimization using pruning and quantization  
   - Real-time ECG anomaly detection with low-power consumption  

---

## 🔹 Repository Contents

- `ECGClassificationwithMachineLearningModels.ipynb` – Step-by-step code for:
  - Data download & preprocessing (MIT-BIH ECG dataset)
  - Normalization, label encoding, train/test split, class balancing using SMOTE
  - Model training & evaluation (Decision Tree, Random Forest, XGBoost, CNN)
  - Results comparison with the original paper  

- `ResearchPaperSummary.pdf` – Self-made summary of the original paper, highlighting:
  - Motivation & contributions
  - Dataset & preprocessing
  - Feature engineering & model selection
  - CNN architecture & training details
  - TinyML optimization: pruning & quantization
  - Deployment setup and performance metrics
  - Discussion and takeaways  

---

## 🔹 Dataset

- **MIT-BIH Arrhythmia Database**  
  - Annotated ECG beats  
  - Five main heartbeat classes:  
    - Normal (N)  
    - Supraventricular (S)  
    - Ventricular (V)  
    - Fusion (F)  
    - Unclassifiable (Q)  
- Preprocessing steps:
  - Band-pass filtering & denoising  
  - Min-max normalization  
  - Segmentation into 200-point windows  
  - Class balancing with SMOTE  

---

## 🔹 Model Summary

| Model           | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) |
|-----------------|-------------|---------------|------------|--------------|
| Decision Tree   | 98.46       | 98.59         | 98.46      | 98.52        |
| Random Forest   | 99.49       | 99.44         | 99.49      | 99.38        |
| XGBoost         | 99.30       | 99.22         | 99.30      | 99.26        |
| CNN             | 98.98       | 99.37         | 98.98      | 99.12        |

> Note: Results were obtained on a subset of the MIT-BIH dataset (5 records) and include SMOTE for class balancing. Differences with the original paper are discussed in the notebook.

---

## 🔹 Key Learnings

- Downloading and preprocessing ECG data, segmenting heartbeats, and labeling classes  
- Importance of normalization, encoding, and train/test splitting  
- SMOTE for handling class imbalance  
- Understanding how Decision Tree, Random Forest, XGBoost, and CNN work  
- Measuring model performance using Accuracy, Precision, Recall, and F1-Score  
- Comparing results with literature to evaluate implementation and understand deviations  
- TinyML concepts: pruning, quantization, and deployment on low-power devices  

---

## 🔹 References

1. M. Hizem, L. Bousbia, Y. Ben Dhiab, M.O.-E. Aoueileyine, R. Bouallegue, **Reliable ECG Anomaly Detection on Edge Devices for Internet of Medical Things Applications**, *Sensors*, 2025. [Link](https://www.mdpi.com/1424-8220/25/8/2496)  
2. MIT-BIH Arrhythmia Database: Moody & Mark, *PhysioNet*  
