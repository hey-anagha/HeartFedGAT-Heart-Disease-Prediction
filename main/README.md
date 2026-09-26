# HeartFedGAT: Explainable Privacy-Preserving Federated Learning for Heart Disease Prediction

HeartFedGAT is an explainable and privacy-preserving federated learning framework for heart disease prediction. The proposed framework integrates a Multi-Scale Convolutional Neural Network (CNN), a Learnable Graph Layer, Graph Attention, encrypted model-update communication, Federated Averaging (FedAvg), and SHAP-based explainability.

## Overview

Heart disease prediction involves heterogeneous clinical attributes that may contain important relationships between patients and features. At the same time, directly sharing medical data across institutions raises privacy concerns.

HeartFedGAT addresses these challenges by performing collaborative model training without requiring the participating clients to share their raw clinical data.

The proposed framework combines:

- Multi-Scale CNN for extracting feature representations at different receptive-field sizes
- Learnable Graph Layer for modeling relationships among features
- Graph Attention for learning feature importance through attention mechanisms
- Federated Learning for collaborative training across multiple clients
- Fernet-based encryption for protecting model updates during transmission
- FedAvg for global model aggregation
- SHAP for model explainability

## Framework

The overall HeartFedGAT workflow is:

```text
Clinical Dataset
       |
       v
Data Preprocessing
       |
       v
Federated Client Partitioning
       |
       +-------------------+
       |                   |
       v                   v
    Client 1            Client 2 ... Client 3
       |                   |
       v                   v
 Multi-Scale CNN      Multi-Scale CNN
       |                   |
       v                   v
 Learnable Graph      Learnable Graph
       |                   |
       v                   v
 Graph Attention      Graph Attention
       |                   |
       v                   v
 Local Model Training
       |
       v
Fernet Encryption of Model Updates
       |
       v
 Server-Side Decryption
       |
       v
 Federated Averaging (FedAvg)
       |
       v
 Global Model
       |
       v
 Heart Disease Prediction
       |
       v
 SHAP Explainability
