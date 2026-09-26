# Main HeartFedGAT Implementation

This directory contains the main implementation of the proposed HeartFedGAT framework for privacy-preserving and explainable heart disease prediction using federated learning.

## Notebook

### `Federated_method.ipynb`

The notebook contains the main federated learning implementation described in the research study.

The implementation includes the major components of the proposed framework:

1. Data preprocessing
2. Feature transformation
3. Multi-Scale CNN
4. Learnable Graph Layer
5. Graph Attention
6. Classification
7. Federated client training
8. Fernet-based model-update encryption
9. Server-side aggregation
10. Federated Averaging (FedAvg)
11. Model evaluation
12. SHAP-based explainability

## Model Architecture

The main HeartFedGAT architecture follows:

```text
Input Features
      |
      v
Multi-Scale CNN
   /       \
Kernel 3  Kernel 5
   \       /
      |
Concatenation
      |
Batch Normalization
      |
Learnable Graph Layer
      |
Graph Attention
      |
Feature Fusion
      |
Residual Connection
      |
Global Average Pooling
      |
Dense (128)
      |
Dense (64)
      |
Sigmoid
      |
Heart Disease Prediction
