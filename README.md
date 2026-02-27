CO₂ Capture Modeling using Artificial Neural Networks (ANN)
Project Overview

This project implements Artificial Neural Network (ANN) models to predict key thermodynamic properties in CO₂ capture systems, inspired by research published in the Journal of Cleaner Production (2025).

Two separate ANN models are developed using TensorFlow/Keras:

🔹 ANN-PCO2 → Predicts CO₂ partial pressure (PCO₂)

🔹 ANN-qabs → Predicts heat of absorption (qabs)

The goal is to reproduce and simulate data-driven modeling for carbon capture processes using deep learning techniques.

**Input Features**

The models use the following experimental parameters:

Temperature (K)

Blending Ratio (wt%)

CO₂ Loading (α, mol CO₂ per mol amine)

These inputs are normalized using Z-score standardization before training.

Model Architecture

Each ANN model consists of:

5 Hidden Layers (64 → 64 → 32 → 16 → 8 neurons)

Sigmoid activation functions

He Normal weight initialization

Adam optimizer (learning rate = 0.001)

Custom combined loss function:

Mean Squared Error (MSE)

Symmetric Mean Absolute Percentage Error (SMAPE)

Early stopping is used to prevent overfitting.

Model Evaluation Metrics

The models are evaluated using:

Mean Squared Error (MSE)

R² Score

SMAPE

Training and validation loss curves are plotted for performance analysis.

**Outputs**

After training, the project generates:

ANN_PCO2_predictions.csv

ANN_qabs_predictions.csv

Each file contains:

Actual values

Predicted values

**Technologies Used:**

Python

TensorFlow / Keras

Scikit-learn

Pandas

Matplotlib

Google Colab

**How to Run:**

Open the notebook in Google Colab.

Upload your dataset in CSV format.

Ensure the dataset contains the required columns:

**Temperature_K**

Blending_ratio_wt_percent

Alpha_mol_CO2_per_mol_amine

PCO2_kPa

qabs_kJ_per_mol_CO2

Run all cells to train and evaluate the models.

**Impact**

Carbon capture is a critical technology for reducing greenhouse gas emissions.
This project demonstrates how machine learning can assist in modeling complex thermodynamic behaviors, reducing the need for extensive experimental work.
