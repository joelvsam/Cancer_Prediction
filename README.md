# Cancer Subtype Prediction from TCGA Gene Expression Data

## Project Overview

This project implements an end-to-end machine learning pipeline to predict breast cancer subtypes (Tumor vs Normal) using TCGA RNA-seq gene expression data. The focus is on model interpretability, feature selection, and biologically meaningful insights.

The workflow is fully reproducible in Google Colab using Python and standard machine learning libraries.

---

## Key Features

- Preprocessing of high-dimensional RNA-seq data (17,814 genes × 590 samples)
- Missing value handling, log transformation, and normalization
- Low-variance gene filtering
- Feature selection to identify top predictive genes
- Classical machine learning models:
  - Logistic Regression
  - Random Forest
- Deep learning model:
  - PyTorch feedforward neural network
- Model evaluation using accuracy, precision, recall, F1-score, and confusion matrices
- Visualization using PCA plots and heatmaps
- Extraction and interpretation of genes contributing to subtype prediction

---

## Dataset

Source: TCGA Breast Cancer (BC-TCGA)

Samples: 590 total  
Tumor samples: 529  
Normal samples: 61  
Genes: 17,814  
Labels: Tumor vs Normal  

Challenges:
- High dimensionality
- Noisy biological data
- Missing values
- Class imbalance

---

## Installation

Install the required Python libraries in **Google Colab** or a **local environment**:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn torch
```

## Usage

- Load the dataset (gene expression data and labels)
- Preprocess the data:
  - Handle missing and infinite values
  - Log-transform expression values
  - Normalize features
  - Remove low-variance genes
- Split the dataset into training and testing sets
- Perform feature selection using:
  - Variance filtering
  - Model-based importance scores
- Train machine learning models:
  - Logistic Regression
  - Random Forest
  - PyTorch feedforward neural network
- Evaluate models using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion matrices
- Interpret results:
  - Extract top predictive genes
  - Visualize expression patterns using PCA and heatmaps

---

## Results

- **Random Forest:** 99% accuracy in Tumor vs Normal classification  
- **Logistic Regression:** 88–95% accuracy depending on preprocessing  
- **PyTorch Feedforward Model:** 95% accuracy  
- **Top Predictive Genes:** Identified using feature importance methods  
- **PCA & Heatmaps:** Clearly separate Tumor and Normal samples

---

## Project Structure

```text
Cancer-Subtype-Prediction/
│
├── README.md
├── Cancer_Subtype_Colab.ipynb
├── data/
│   ├── BC-TCGA-Normal.txt
│   ├── BC-TCGA-Tumor.txt
│   └── (additional datasets)
```


## Future Work

- Extend the pipeline to multi-omics datasets for improved subtype prediction  
- Integrate drug response or clinical outcome data  
- Deploy the interpretable machine learning pipeline as a clinical decision support tool  

