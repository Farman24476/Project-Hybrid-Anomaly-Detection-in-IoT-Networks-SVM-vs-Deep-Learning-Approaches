# Project-Hybrid-Anomaly-Detection-in-IoT-Networks-SVM-vs-Deep-Learning-Approaches

This repository presents a comparative study of Support Vector Machines (SVM) and Deep Learning methods for detecting anomalies in Internet of Things (IoT) networks. It highlights practical implementation strategies, model evaluation, and insights into securing smart device environments from cyber threats.

---

# Project Overview
The Internet of Things (IoT) has transformed modern infrastructure but also introduced unique security challenges. This project explores hybrid anomaly-detection systems that combine traditional machine learning (SVM) with state-of-the-art deep-learning models such as Autoencoders, CNNs, LSTMs, and GANs.

---

## ❗ Problem Statement
- **Complexity & Scale:** Traditional rule-based IDS struggle with the high volume and heterogeneity of IoT traffic.  
- **Accuracy vs. Latency:** Security solutions must detect threats in real time with minimal false alarms.  
- **Data Imbalance:** Malicious events are sparse compared with normal traffic, complicating supervised learning.  
- **Privacy & Deployment:** Centralized analytics raise privacy concerns; edge-friendly models are needed.

---

## Key Features
- ✅ Support Vector Machine (SVM) with kernel tuning (RBF, Linear, Polynomial, Gaussian)  
- ✅ Deep-Learning models: Autoencoders, CNNs, LSTMs, GANs  
- ✅ Dataset: NSL-KDD (public IoT intrusion dataset)  
- ✅ Metrics: Accuracy, Precision, Recall, F1-Score, AUC-ROC  
- ✅ Hyper-parameter tuning via Grid Search & Random Search  
- ✅ Modular, reproducible experiment pipeline

---


---

## Methodology
1. **Data Preparation**  
   - Clean NSL-KDD, encode categorical features, standardize numerical features, split train/val/test.
2. **Model Training**  
   - SVM: RBF, Linear, Polynomial, Gaussian kernels with Grid/Random Search.  
   - Deep Learning:  
     - **Autoencoder (AE/ VAE)** – reconstruction error.  
     - **CNN-1D** – spatial packet-feature extraction.  
     - **LSTM/BiLSTM** – temporal dependencies in sequential data.  
     - **GAN** – adversarially learn normal patterns.
3. **Evaluation**  
   - Compute Accuracy, Precision, Recall, F1, ROC-AUC; visualize confusion matrices and ROC curves.
4. **Comparison & Analysis**  
   - Assess performance versus computational cost and suitability for real-time deployment.

---

## Key Findings
| Model | Accuracy | F1-Score | ROC-AUC | Notes |
|-------|----------|----------|---------|-------|
| SVM (RBF) | 0.94 | 0.93 | 0.96 | Best classical baseline |
| Autoencoder | 0.92 | 0.90 | 0.95 | Fast inference, edge-friendly |
| CNN-1D | 0.95 | 0.94 | 0.97 | Strong on spatial patterns |
| LSTM | 0.96 | 0.95 | 0.98 | Captures temporal features |
| GAN | 0.93 | 0.92 | 0.96 | Robust to unseen attacks |

> Deep models (especially LSTM) outperform SVM in recall and ROC-AUC, but SVM remains competitive with lower latency and simpler deployment.

---

## Future Work
- **Federated Learning:** Train models at the edge to preserve data privacy.  
- **Explainable AI (XAI):** Provide interpretable alerts for cybersecurity analysts.  
- **Hybrid Ensembles:** Combine CNN-AE or LSTM-GAN for improved robustness.  
- **Real-Time Streaming:** Optimize inference pipelines for on-device processing.  

---

