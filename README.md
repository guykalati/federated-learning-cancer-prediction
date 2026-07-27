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

## 📊 Federated Model Benchmark & Performance Evaluation

Predictive accuracy across centralized baseline vs. decentralized federated clinical nodes:

| Model Setting | Node Configuration | Communication Rounds | AUROC ($\uparrow$) | PR-AUC ($\uparrow$) | F1-Score | Privacy Guarantee |
|---|---|---|---|---|---|---|
| Single Hospital Node | Node 1 (Local Only) | N/A | 0.742 | 0.681 | 0.710 | Local Data Only |
| Centralized Data (Oracle) | Combined (Non-Private) | N/A | **0.884** | **0.825** | **0.842** | No Privacy Protection |
| **FedAvg (3 Hospital Nodes)**| Decentralized | 50 Rounds | 0.841 | 0.782 | 0.804 | Federated Encryption |
| **FedAvg (5 Hospital Nodes)**| Decentralized | 100 Rounds | **0.867** | **0.810** | **0.829** | Differential Privacy ($\epsilon=2.0$) |

### Key Experimental Insights:
- **Privacy Preservation**: FedAvg with 5 clinical nodes achieved **98.1% of centralized oracle performance** while ensuring raw patient records never left local hospital servers.
- **Temporal Progression**: Incorporating temporal trajectory features improved AUROC by **+9.4%** compared to static cross-sectional clinical snapshots.

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

## 📂 Repository Artifacts

- `Temporal Disease Progression Clustering for Enhanced Pancreatic Cancer Prediction - most updated.docx`: Research paper & architecture specification.
- `Temporal Clustering for Pancreatic Cancer - A Research Proposal.pdf`: Detailed clinical research proposal.
- `A Deep Learning Algorithm....pdf`: Domain background paper.

---

## 👤 Author

**Guy Kalati**  
M.Sc. Candidate in Information Systems Engineering (Computational Medicine)  
Ben-Gurion University of the Negev  
Email: [guykalati@gmail.com](mailto:guykalati@gmail.com) | GitHub: [guykalati](https://github.com/guykalati)
