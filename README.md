# AI-Driven Adaptive Intrusion Detection and Network Threat Intelligence Framework using Transformer-Based Temporal Anomaly Detection

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![License](https://img.shields.io/badge/License-Academic-green.svg)
![Status](https://img.shields.io/badge/Status-Research-success.svg)

---

## Overview

Modern cyberattacks exhibit complex temporal and behavioral patterns that are difficult to detect using traditional signature-based Intrusion Detection Systems (IDS). While machine learning-based IDS solutions improve detection accuracy, they often lack interpretability and actionable threat intelligence.

This project presents an **AI-Driven Adaptive Intrusion Detection and Network Threat Intelligence Framework** that combines:

- Transformer-Based Temporal Anomaly Detection
- Hybrid Temporal Representation Engineering (HTRE)
- Explainable Artificial Intelligence (SHAP)
- Automated Threat Intelligence Engine

The framework not only detects multiple categories of cyberattacks but also explains **why** a prediction was made and generates an intelligence-driven threat assessment including:

- Threat Severity
- Risk Score
- MITRE ATT&CK Mapping
- Priority Level
- Security Recommendations

---

# Framework Architecture

```text
                         CICIDS2018 Dataset
                                 │
                                 ▼
                     Data Preprocessing
                                 │
                                 ▼
      Hybrid Temporal Representation Engineering (HTRE)
                                 │
                                 ▼
      Transformer-Based Temporal Anomaly Detection
                                 │
                                 ▼
               Multi-Class Attack Prediction
                                 │
                                 ▼
                  SHAP Explainability Engine
                                 │
                                 ▼
              Threat Intelligence Framework
                                 │
                                 ▼
          Comprehensive Threat Assessment Report
```

---

# Project Objectives

The proposed framework aims to:

- Detect multiple categories of network attacks using a Transformer architecture.
- Improve detection accuracy through temporal feature engineering.
- Provide transparent AI predictions using SHAP.
- Convert IDS predictions into actionable cyber threat intelligence.
- Assist security analysts through automated risk assessment and mitigation recommendations.

---

# Dataset

The framework is developed using the **CICIDS2018 Dataset**.

## Dataset Characteristics

- Realistic enterprise network traffic
- Benign and malicious network flows
- Modern attack scenarios
- Flow-based statistical features
- Multi-class attack labels

> **Note:**  
> The dataset is not included in this repository due to licensing restrictions and repository size limitations.

---

# Attack Classes

| Attack Type |
|-------------|
| Benign |
| DDoS |
| DoS Hulk |
| DoS GoldenEye |
| DoS Slowloris |
| DoS SlowHTTPTest |
| Bot |
| FTP-Patator |
| SSH-Patator |
| PortScan |
| Web Attack – Brute Force |
| Web Attack – XSS |
| Web Attack – SQL Injection |
| Heartbleed |
| Infiltration |

---

# Proposed Methodology

The proposed framework consists of four major stages.

---

## Stage 1 — Data Preprocessing

The CICIDS2018 dataset undergoes preprocessing to prepare high-quality inputs for deep learning.

### Preprocessing Pipeline

- Missing value handling
- Infinite value removal
- Duplicate removal
- Label encoding
- Feature normalization
- Train-test split

---

## Stage 2 — Hybrid Temporal Representation Engineering (HTRE)

Instead of relying solely on the original network flow statistics, the framework introduces additional temporal representations that better capture network behaviour.

### Original Network Features

Examples include:

- Flow Duration
- Total Forward Packets
- Total Backward Packets
- Flow Bytes/s
- Flow Packets/s
- Packet Length Statistics
- Inter Arrival Time (IAT)
- TCP Flag Statistics
- Window Size Features
- Active/Idle Time

...and 69 additional flow features.

---

### Proposed HTRE Features

| Feature | Description |
|----------|-------------|
| TRE_LogFlowBytes | Logarithmic representation of flow bytes |
| TRE_LogFlowBytesChange | Temporal variation in transmitted bytes |
| TRE_FlowRate | Normalized traffic flow rate |
| TRE_PacketRate | Packet transmission dynamics |
| TRE_BurstScore | Burst behaviour indicator |
| TRE_IATVariation | Inter-arrival time variation |

These engineered features allow the Transformer model to learn temporal behaviour more effectively than raw flow statistics alone.

---

## Stage 3 — Transformer-Based Temporal Anomaly Detection

The proposed IDS utilizes a Transformer architecture specifically adapted for sequential network traffic analysis.

### Detection Pipeline

```text
Input Features
      │
      ▼
Feature Normalization
      │
      ▼
HTRE Feature Integration
      │
      ▼
Feature Embedding
      │
      ▼
Positional Encoding
      │
      ▼
Multi-Head Self Attention
      │
      ▼
Feed Forward Network
      │
      ▼
Dropout + Layer Normalization
      │
      ▼
Dense Classification Layer
      │
      ▼
Softmax Output
      │
      ▼
Attack Prediction
```

### Transformer Components

- Feature Embedding
- Positional Encoding
- Multi-Head Self Attention
- Feed Forward Network
- Residual Connections
- Layer Normalization
- Dropout
- Dense Classification Layer
- Softmax Output Layer

---

## Stage 4 — Explainable AI (SHAP)

Deep learning models are often considered black boxes.

To improve interpretability, SHAP (SHapley Additive exPlanations) is integrated into the framework.

The explainability module provides:

- Global Feature Importance
- Class-wise Feature Importance
- Local Prediction Explanation
- Top Influential Features

### Generated Outputs

- SHAP Summary Plot
- Feature Importance CSV
- Class-wise Rankings
- Local Explanation Analysis

---

# Threat Intelligence Framework

Instead of stopping at attack classification, the proposed framework transforms IDS predictions into actionable cyber threat intelligence.

## Threat Intelligence Pipeline

```text
Predicted Attack
       │
       ▼
Knowledge Base Lookup
       │
       ▼
Severity Assessment
       │
       ▼
Risk Score Calculation
       │
       ▼
Risk Classification
       │
       ▼
Priority Assignment
       │
       ▼
MITRE ATT&CK Mapping
       │
       ▼
Security Recommendations
       │
       ▼
Threat Assessment Report
```

---

# Generated Threat Report

The framework automatically generates:

- Predicted Attack
- Confidence Score
- Attack Category
- Attack Description
- SHAP Feature Explanation
- Threat Severity
- Risk Score
- Risk Level
- Priority Level
- MITRE ATT&CK Technique
- Recommended Mitigation Actions

---

## Example Threat Report

```text
Prediction        : SQL Injection

Confidence        : 96.8%

Category          : Web Application Attack

Description       : SQL statements injected into application inputs to manipulate backend databases.

Top SHAP Features

• Fwd Packet Length Mean
• Fwd Segment Size Min
• TRE_LogFlowBytesChange
• Init Bwd Window Bytes
• Fwd Packet Length Max

Severity          : Critical

Risk Score        : 96.8

Risk Level        : Critical

Priority          : P1

MITRE ATT&CK

T1190 - Exploit Public-Facing Application

Recommendations

1. Inspect web server logs.
2. Validate application input filtering.
3. Apply security patches.
4. Update WAF rules.
```

---

# Key Contributions

- Transformer-Based Intrusion Detection
- Hybrid Temporal Representation Engineering (HTRE)
- Enhanced Temporal Feature Learning
- SHAP-Based Explainable AI
- Class-wise Feature Attribution
- Automated Threat Intelligence Generation
- MITRE ATT&CK Integration
- Risk-Based Threat Prioritization
- Automated Security Recommendations
- Human-Readable Threat Assessment Reports

---

# Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- SHAP
- Matplotlib
- Seaborn

---

# Installation

```bash
git clone https://github.com/<username>/<repository>.git

cd <repository>

pip install -r requirements.txt
```

---

# Project Structure

```text
├── Dataset/
├── notebooks/
│   ├── transformer-model-ids.ipynb
│   ├── xai-ids.ipynb
│   └── ids-18.ipynb
├── models/
├── outputs/
│   ├── SHAP/
│   ├── Reports/
│   └── Figures/
├── requirements.txt
└── README.md
```

---

# Future Work

- Real-time Network Traffic Monitoring
- Federated Intrusion Detection
- Graph Neural Networks
- Online Continual Learning
- Threat Intelligence Sharing
- Integration with SIEM Platforms

---

# License

This project is intended for **academic research and educational purposes**.

---

# Citation

If you use this work in your research, please cite the associated thesis or future publication.

```bibtex
@misc{AI_IDS_Framework,
  title={AI-Driven Adaptive Intrusion Detection and Network Threat Intelligence Framework using Transformer-Based Temporal Anomaly Detection},
  author={Revanth Kengana},
  year={2026}
}
```

---

## Author

**Revanth Kengana**

Cybersecurity Research | AI for Cyber Defense | Intrusion Detection | Explainable AI
