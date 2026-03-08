# LNUQNet: Lithology Neural Uncertainty Quantification Network

## Overview

LNUQNet (Lithology Neural Uncertainty Quantification Network) is an uncertainty-aware deep learning framework designed for automated lithology classification with predictive uncertainty estimation.
The model integrates convolutional neural network (CNN) feature extraction with transformer-based contextual learning to capture both local geological patterns and global stratigraphic dependencies.

To quantify predictive uncertainty, the framework employs Monte Carlo Dropout during inference, enabling probabilistic lithology predictions that can support more reliable geological interpretation.

This repository contains the code, trained model, and sample dataset used to develop and evaluate LNUQNet.

---

## Repository Structure

LNUQNet/

* notebooks/

  * LNUQNet_1_RBHS.ipynb – Rule-Based Hierarchical System pipeline
  * LNUQNet_1_Model.ipynb – Model architecture definition and training
  * LNUQNet_3_Uncertainty Quantification & Plots.ipynb – Prediction, uncertainty estimation, and visualization

* models/

  * best_lnuqnet_model.keras – Trained LNUQNet model

* data/

  * All 12 datasets used.
    
* requirements.txt – Python dependencies required to run the notebooks

---

## Installation

Install the required Python packages:

pip install -r requirements.txt

---

## Usage

Run the notebooks sequentially:

1. **LNUQNet_1_RBHS.ipynb**

   * Ground Truth Generation
   * Dataset preparation

2. **LNUQNet_2_Model.ipynb**

   * LNUQNet architecture implementation
   * Model training

3. **LNUQNet_3_Uncertainty Quantification & Plots.ipynb**

   * Lithology prediction
   * Monte Carlo dropout uncertainty estimation
   * Visualization of results

---

## Model Description

The LNUQNet architecture combines:

* Convolutional neural networks for local lithological feature extraction
* Transformer-based attention mechanisms for capturing depth-wise contextual relationships
* Monte Carlo Dropout for uncertainty quantification

This hybrid design enables robust lithology prediction while providing confidence estimates for each classification.

---

## Data

All datasets have been provided in the data folder.

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
"LNUQNet: An Uncertainty-Aware Deep Learning Model for 
Lithology Classification"
