# Histopathologic Cancer Detection — Kaggle Competition

## Overview

This project is part of the **Kaggle competition** on detecting **metastatic cancer** in histopathologic image patches. The objective is to build a model that classifies small 96x96 pixel RGB images as either containing cancerous (metastatic) tissue or not — a **binary classification** problem.

## Dataset Description

- **Training set**: 220,025 labeled images
- **Test set**: 57,458 unlabeled images
- **Labels**: `1` for metastatic cancer present, `0` for absent
- **Metric**: Area Under the ROC Curve (**AUC**)

## Approach

This project focused on building Convolutional Neural Network (**CNN**) models to analyze image data. The process included:

- Image preprocessing and normalization
- Model architecture design (Conv layers, pooling, dropout)
- Regularization (dropout, batch normalization)
- Model tuning (learning rate, batch size, epochs)
- Evaluation using validation accuracy and AUC
- Submission to Kaggle for final scoring

##  Models Tried

We experimented with multiple CNN variants, exploring:
- Different depths (2–5 convolutional layers)
- Dropout rates (0.2 to 0.5)
- Learning rate schedules and early stopping
- Regularized vs non-regularized versions

## Final Model Selection

After submitting various models to Kaggle, we compared both **public and private AUC scores**. While Model #5 had the highest public score, **Model #4 offered the best combination of public and private scores**, suggesting stronger generalization.

| Model     | Public AUC | Private AUC | Notes                          |
|-----------|------------|-------------|--------------------------------|
| Model #4  | 0.8694     | **0.8298**  | Final model — best balance  |
| Model #5  | **0.8699** | 0.8098      | High public, lower private AUC |
| Others    | —          | —           | Lower performance overall      |

