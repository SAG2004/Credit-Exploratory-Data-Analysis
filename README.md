# 📊 Loan Application EDA & Preprocessing Pipeline

## 📝 Project Overview

This repository contains a robust data engineering and exploratory data analysis (EDA) pipeline designed to preprocess complex financial records for downstream machine learning. The project processes a large-scale loan application dataset (**307,511 records, 122 features**) to identify risk patterns, resolve data quality anomalies, and extract high-signal features for predicting loan default rates.

## 🎯 Key Objectives

* **Data Cleansing:** Evaluate structural integrity and optimize feature space by removing high-sparsity columns.
* **Robust Imputation:** Handle missing values across numerical and heavy-tailed categorical variables without distorting underlying statistical distributions.
* **Feature Engineering:** Transform temporal and continuous metrics into interpretable, standardized formats.
* **Risk Profiling:** Perform univariate and bivariate analysis to quantify class imbalances and isolate baseline risk indicators.

---

## 🛠️ Pipeline Architecture & Methodology

### 1. Dimensionality Reduction & Quality Control

* **Sparsity Optimization:** Engineered a dynamic thresholding function to identify and drop columns containing more than **47% missing values**.
* **Feature Space Reduction:** Successfully reduced the dataset from 122 noisy features to **73 high-signal columns**, significantly decreasing memory overhead and computational complexity.

### 2. Strategic Data Imputation

* **Continuous Variables:** Executed median-based imputation for heavily skewed numerical features (e.g., `EXT_SOURCE_3`, bureau inquiry metrics) to neutralize outlier distortion.
* **Categorical Variables:**
* Addressed a 31% data gap in the `OCCUPATION_TYPE` column by aggregating missing records into a unified `Others` category to preserve statistical weight.
* Applied mode imputation for remaining low-cardinality categorical gaps.



### 3. Feature Engineering & Discretization

* **Temporal Standardization:** Transformed negative, day-based legacy metrics (`DAYS_BIRTH`, `DAYS_EMPLOYED`, `DAYS_REGISTRATION`) into absolute, human-readable yearly values (`YEARS_BIRTH`, etc.).
* **Data Binning:** Discretized continuous numerical features into logical brackets to enhance model interpretability:
* **Age Brackets:** Segmented into demographic tiers (e.g., `25-45`, `45-65`).
* **Credit Tiers:** Segmented `AMT_CREDIT` into ordinal categories (e.g., `Low Credit`, `Very High Credit`).



### 4. Class Imbalance Profiling (Target Variable)

Segmented the dataset based on the `TARGET` variable to conduct isolated analyses on defaulters versus non-defaulters.

* **Non-Defaulters:** ~91.9% of the dataset.
* **Defaulters:** ~8.07% of the dataset.
* *Note: This severe imbalance establishes the baseline for SMOTE or weighted loss functions in the upcoming predictive modeling phase.*

---

## 💻 Technology Stack

* **Languages:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib.pyplot`, `seaborn`
* **Environment:** Jupyter Notebook / IPython

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python installed along with the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter

```

### Execution

1. Clone this repository:
```bash
git clone https://github.com/yourusername/loan-application-eda.git

```


2. Navigate to the project directory:
```bash
cd loan-application-eda

```


3. Launch the Jupyter Notebook:
```bash
jupyter notebook EDA_Preprocessing_Pipeline.ipynb

```



---

## 🔮 Future Scope

Phase 2 of this project will transition from data engineering to predictive modeling, utilizing the cleaned 73-feature dataset to train classification models (Logistic Regression, Random Forest, XGBoost) and implementing handling techniques (like SMOTE) for the 91:8 class imbalance.
