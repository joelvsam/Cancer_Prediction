Cancer Subtype Prediction from TCGA Gene Expression Data
Project Overview

This project implements an end-to-end machine learning pipeline to predict breast cancer subtypes using TCGA RNA-seq gene expression data. The focus is on interpretable models, feature selection, and biologically meaningful insights. The workflow is fully reproducible in Google Colab using Python and standard ML libraries.

Features

Preprocessing of high-dimensional RNA-seq data (17,814 genes × 590 samples)

Missing value handling, log-transform, and variance filtering

Feature selection to identify top predictive genes

Classical ML models: Logistic Regression, Random Forest

PyTorch feedforward model for supervised classification

Visualization of results using PCA and heatmaps

Extraction of top genes contributing to subtype prediction

Evaluation with accuracy, precision, recall, F1-score, and confusion matrices

Dataset

Source: TCGA Breast Cancer (BC-TCGA) dataset

Samples: 590 (529 tumor, 61 normal)

Genes: 17,814

Labels: Tumor vs Normal

Challenges: High dimensionality, noise, missing values

Installation

Install required Python libraries in Google Colab:

!pip install pandas numpy scikit-learn matplotlib seaborn torch

Usage

Load the dataset (expression data and labels)

Preprocess data: handle missing values, log-transform, normalize, remove low-variance genes

Split into training and testing sets

Feature selection using variance filtering and importance scores

Train models: Logistic Regression, Random Forest, PyTorch feedforward network

Evaluate models using accuracy, precision, recall, F1-score, and confusion matrices

Interpret results: extract top predictive genes and visualize expression patterns

Results

Random Forest: 99% accuracy in tumor vs normal classification

Logistic Regression: 88–95% accuracy depending on preprocessing

PyTorch feedforward model: 95% accuracy

Top predictive genes: identified using feature importance

PCA & heatmaps: clearly separate tumor and normal samples

File Structure
Cancer-Subtype-Prediction/
│
├─ README.md                 # Project documentation
├─ Cancer_Subtype_Colab.ipynb # Full Colab notebook with end-to-end pipeline
├─ data/
│   ├─ BC-TCGA-Normal.txt
│   ├─ BC-TCGA-Tumor.txt
│   └─ (other datasets)

Future Work

Extend to multi-omics datasets for improved subtype prediction

Integrate drug response or clinical outcome data

Deploy interpretable ML pipeline as a clinical decision support tool
