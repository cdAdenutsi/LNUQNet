# LNUQNet: Lithology Neural Uncertainty Quantification Network

## Overview

LNUQNet (Lithology Neural Uncertainty Quantification Network) is an uncertainty-aware deep learning framework designed for automated lithology classification with predictive uncertainty estimation.
The model integrates convolutional neural network (CNN) feature extraction with transformer-based contextual learning to capture both local geological patterns and global stratigraphic dependencies.

To quantify predictive uncertainty, the framework employs Monte Carlo Dropout during inference, enabling probabilistic lithology predictions that can support more reliable geological interpretation.

This repository contains the code, trained model, and datasets used to develop and evaluate LNUQNet.

---

## Repository Structure

LNUQNet/

* notebooks/

  * LNUQNet_1_RBHS.ipynb – Rule-Based Hierarchical System (RBHS) pipeline for generating ground truth labels
  * LNUQNet_2_Model.ipynb – Model architecture definition and training
  * LNUQNet_3_Uncertainty_Quantification_and_Plots.ipynb – Prediction, uncertainty estimation, and visualization

* models/

  * best_lnuqnet_model.keras – Trained LNUQNet model

* data/

  * Contains the 12 datasets used for model development and evaluation

* figures/

  * RBHS_framework.png
  * cnn_architecture.png
  * depthwise_self_attention.png

* requirements.txt – Python dependencies required to run the notebooks

---

## Installation

Install the required Python packages:

pip install -r requirements.txt

---

## Usage

Run the notebooks sequentially:

1. **LNUQNet_1_RBHS.ipynb**

* Ground truth generation using the Rule-Based Hierarchical System (RBHS)
* Dataset preparation

2. **LNUQNet_2_Model.ipynb**

* Implementation of the LNUQNet architecture
* Model training

3. **LNUQNet_3_Uncertainty_Quantification_and_Plots.ipynb**

* Lithology prediction
* Monte Carlo Dropout uncertainty estimation
* Visualization of predictions and uncertainty

---

## Model Architecture

### RBHS Ground Truth Generation Framework

![RBHS Framework](figures/RBHS.png)

The Rule-Based Hierarchical System (RBHS) is used to generate structured lithology labels from well log measurements. This framework encodes geological domain knowledge through hierarchical decision rules to produce consistent training labels.

---

### CNN Feature Extraction Architecture

![CNN Architecture](figures/Cnn_Architecture.png)

The CNN component extracts local lithological patterns from well log features. Convolutional layers capture spatial relationships within the input feature window.

---

### Depthwise Self-Attention Mechanism

![Depthwise Self Attention](figures/Depth-wise_Self_Attention.png)

The transformer-based depthwise self-attention mechanism captures long-range depth dependencies within the well log sequence, enabling the model to learn stratigraphic context.

---

## Model Description

The LNUQNet architecture combines:

* Convolutional neural networks for local lithological feature extraction
* Transformer-based attention mechanisms for capturing depth-wise contextual relationships
* Monte Carlo Dropout for uncertainty quantification

This hybrid design enables robust lithology prediction while providing confidence estimates for each classification.

---

## Results

LNUQNet demonstrates strong lithology classification performance while providing uncertainty estimates for each prediction.

Example evaluation results from the trained model include:

| Metric           | Value            |
| ---------------- | ---------------- |
| Overall Accuracy | (add from paper) |
| Precision        | (add from paper) |
| Recall           | (add from paper) |
| F1 Score         | (add from paper) |

The uncertainty estimation allows identification of low-confidence predictions, which is valuable for geological interpretation and quality control in automated lithology classification.

---

## Data

All datasets used in the study are provided in the **data/** folder.

---

## Reproducibility

To reproduce the results:

1. Install dependencies
2. Run the notebooks sequentially
3. Use the provided trained model or retrain using the training notebook

---

## Citation

If you use this code in your research, please cite:

Author(s).
"LNUQNet: An Uncertainty-Aware Deep Learning Model for Lithology Classification."
