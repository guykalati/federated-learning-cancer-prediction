# Federated Learning & Temporal Progression Clustering for Cancer Risk Prediction

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange.svg)
![Federated Learning](https://img.shields.io/badge/Federated-Learning-purple.svg)
![Healthcare AI](https://img.shields.io/badge/Domain-Healthcare%20AI-red.svg)

A machine learning framework combining privacy-preserving **Federated Learning** with **temporal progression clustering** to predict metastatic and pancreatic cancer risk from longitudinal patient data. Built using data from the WiDS Datathon challenge and clinical patient progression benchmarks.

---

## 🔬 Clinical Motivation & Architecture

Patient data across multiple hospital sites cannot easily be centralized due to strict privacy regulations (HIPAA/GDPR). This framework enables collaborative model training across decentralized clinical nodes using federated aggregation algorithms (FedAvg) while preserving patient privacy.

```
Hospital Node 1 (Local EHR) ──┐
Hospital Node 2 (Local EHR) ──┼──➔ Federated Server (FedAvg) ──➔ Global Cancer Risk Model
Hospital Node 3 (Local EHR) ──┘
```

---

## ⭐ Key Features

- **Federated Model Aggregation**: Decentralized model updates using Federated Averaging (FedAvg) across simulated clinical clients.
- **Longitudinal Feature Modeling**: Captures patient disease progression timelines, treatment histories, and demographic risk factors.
- **Privacy-Preserving Architecture**: Prevents raw patient EHR exposure while maintaining high predictive performance (AUROC / F1-score).

---

## 🛠 Tech Stack

- **ML & DL Frameworks**: PyTorch, Scikit-learn, PySyft / Federated utilities
- **Data Analysis**: Pandas, NumPy, SciPy
- **Evaluation**: ROC-AUC curves, PR-AUC, confusion matrices, SHAP interpretability

---

## 👤 Author

**Guy Kalati**  
M.Sc. Candidate in Information Systems Engineering (Computational Medicine)  
Ben-Gurion University of the Negev  
Email: [guykalati@gmail.com](mailto:guykalati@gmail.com) | GitHub: [guykalati](https://github.com/guykalati)
