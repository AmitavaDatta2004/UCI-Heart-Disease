<div align="center">
  <h1>🫀 UCI Heart Disease: Data Mining & Knowledge Discovery</h1>
  <p><i>A comprehensive data mining pipeline predicting and analyzing heart disease risk factors.</i></p>

<!-- Badges -->

<img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn" />
  <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" alt="Matplotlib" />
</div>

<br/>

## 📖 Overview

This repository contains a Mini Project for the **Data Mining (PEC-AIML601B)** course. It demonstrates a full end-to-end data mining and preprocessing pipeline applied to the well-known **[UCI Heart Disease (Cleveland) dataset](https://archive.ics.uci.edu/ml/datasets/heart+disease)**.

The primary goal is to extract meaningful clinical insights, handle imperfect real-world data, and build interpretable predictive models that could assist healthcare professionals in screening and resource allocation.

## ✨ Pipeline Phases

The project is heavily structured into 7 distinct phases mimicking a real-world data science workflow:

1. **Object & Attribute Definition** 📊 Classifying the 14 attributes into meaningful statistical types (nominal, ordinal, ratio, binary).
2. **Exploratory Data Analysis (EDA)** 🔍 Understanding distributions, detecting class imbalances, and visualizing attribute correlations via heatmaps and boxplots.
3. **Similarity & Association Analysis** 🔗 \
   - Correlation: Comparing *Pearson (linear)* vs. *Spearman (rank)*.
   - Patient Similarity: Generating matrices using *Euclidean*, *Cosine*, and *Jaccard* distances.
4. **Data Quality Assessment** 🛠️ Identifying missing data mechanisms using `missingno`, and detecting statistical outliers comprehensively using the IQR method.
5. **Missing Value Handling** 🩹 Evaluating multiple strategies: *Mean*, *Median*, *KNN (k=5)*, and *Iterative Imputation (MICE)*.
6. **Preprocessing & Modeling** ⚙️ Securing the workflow with `sklearn.pipeline.Pipeline` to prevent data leakage during scaling and Logistic Regression modeling.
7. **Knowledge Discovery** 💡 
   Translating mathematical coefficients into actionable healthcare decisions and profiling high-risk patient subgroups.

## 📂 Repository Structure

```text
📁 UCI Heart Disease/
├── 📄 heart_disease_analysis.ipynb # Interactive Jupyter Notebook analysis
├── 📂 outputs/                  # Generated plots, heatmaps, and visuals
└── 📄 README.md                 # Project documentation
```

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.x installed along with the required analytical libraries. You can install them manually via pip:

```bash
pip install pandas numpy matplotlib seaborn missingno scikit-learn scipy
```

### Running the Analysis

Run the interactive Jupyter Notebook to explore the data, reproduce the pipeline steps, and visualize results directly.

```bash
jupyter notebook heart_disease_analysis.ipynb
```

## 🧠 Key Clinical Insights Discovered

- **Strongest Predictors**: `thal` (Thalassemia), `ca` (Number of major vessels colored by fluoroscopy), `cp` (Chest pain type), and `thalach` (Maximum heart rate achieved).
- **Risk Profile**: Patients diagnosed with heart disease generally exhibit a lower maximum heart rate (~ 139 bpm vs. 158 bpm) and higher ST depression (`oldpeak`). More frequent occurrence of asymptomatic chest pain is a severe risk marker.
- **Redundant Attributes**: `fbs` (fasting blood sugar) and `trestbps` (resting blood pressure) showed near-zero linear and ranked correlation to heart disease presence in this specific cohort.
- **Imputation Impact**: Utilizing KNN Imputation allowed us to retain all records gracefully rather than dropping data, which is crucial in clinical datasets with limited samples.

---

*Developed for Knowledge Discovery & Healthcare Analytics.*
