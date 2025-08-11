# Comparative Analysis of KNN and DNN for Spreading Factor Prediction in LoRaWAN Networks

This repository contains the implementation and results of our project, **"Comparative Analysis of KNN and DNN for Spreading Factor Prediction in LoRaWAN Networks"**, inspired by the AI-ERA framework proposed by **Dr Arshad Farhad** and **Jae-Young Pyun**.

## 📌 Overview
In LoRaWAN-based IoT networks, selecting the optimal **Spreading Factor (SF)** is essential for balancing range, data rate, and energy efficiency.  
While the original **AI-ERA** approach used a **Deep Neural Network (DNN)**, we explored a **K-Nearest Neighbors (KNN)** alternative to improve accuracy and reduce computational cost.

## 🔍 Methodology
- Replicated the AI-ERA data preprocessing pipeline using **ns-3 simulation datasets**.
- Input features: Device coordinates (X, Y), Received Power (RxPw), Signal-to-Noise Ratio (SNR).
- Labels: Average Spreading Factor (SF7–SF12) per device group.
- Models tested:
  - **KNN (k=3)**
  - **DNN (AI-ERA original)**
  - Random Forest (baseline comparison)

## 📊 Results
| Metric            | KNN    | DNN (AI-ERA) |
|-------------------|--------|--------------|
| Accuracy          | **72.6%** | 55.2%        |
| F1 Score (Weighted)| **72.3%** | 52.5%        |
| Training Time     | N/A    | ~12.4s        |
| Inference Time    | 0.004s | 0.0006s       |

**Key Takeaways:**
- **KNN** outperformed **DNN** in accuracy and F1-score.
- Simpler models like KNN can be more practical for **edge IoT deployments**.
- SNR and Received Power were the most influential features for SF prediction.


