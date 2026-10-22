# Credit Risk EDA 📊
Exploratory Data Analysis of credit applications to uncover patterns in loan defaults and repayment behavior.

## 📑 Table of Contents
- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Tech Stack](#-tech-stack)
- [Future Improvements](#-future-improvements)
- [License](#-license)
- [Contact](#-contact)

## 🔎 Overview
This project analyzes loan application data to understand factors influencing repayment difficulties. Using Exploratory Data Analysis (EDA), the study identifies risk drivers in consumer lending and provides insights into creditworthiness.

The repository provides:
- A structured EDA workflow (data cleaning, outlier detection, univariate & bivariate analysis).
- Identification of default risk patterns in applicant profiles.
- Visualizations of correlations and trends across socio-economic & loan-related variables.

## ✨ Features

- **Outlier Analysis:** Detect anomalies in income, loan amounts, and demographic data.
- **Target Variable Imbalance Check:** Assess distribution of repayment vs. default cases.
- **Univariate & Bivariate Analysis:** Examine categorical and numerical drivers of default.
- **Correlation Analysis:** Identify strong predictor variables.
- **Risk Profiling:** Highlight applicant categories more likely to repay or default.

## 📂 Project Structure
credit-risk-eda/

| File                 | Description                          |
|---------------------------------|--------------------------------------|
| `application_data.csv`           | Client details at loan application   |
| `previous_application.csv`       | Records of previous loans            |
| `columns_description.csv`        | Data dictionary                       |
| `credit_eda.ipynb`               | Full EDA notebook                     |
| `requirements.txt`               | Dependencies                           |
| `README.md`                      | Project documentation                 |

## ⚡ Getting Started
1. Clone the repository:
```bash
git clone https://github.com/Kashvi1811/Credit-EDA/.git
cd Credit-EDA
````

2. (Optional) Create a virtual environment:

```bash
python -m venv env
source env/bin/activate       # macOS / Linux
env\Scripts\activate          # Windows PowerShell
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## 🖥️ Usage

- Open the Jupyter Notebook:
jupyter notebook notebooks/credit_eda.ipynb

- Run the notebook step by step to explore:
- Data cleaning & preprocessing.
- Outlier detection & imbalance analysis.
- Univariate, bivariate, and correlation analyses.
- Risk segmentation of applicants.

## 🛠 Tech Stack

* Python, Jupyter
* pandas, NumPy
* Matplotlib, Seaborn
* scikit-learn (for preprocessing support)

## 🚀 Future Improvements

* Extend analysis with **predictive modeling** (Logistic Regression, XGBoost, etc.).
* Address **class imbalance** using SMOTE or weighted models.
* Build a **credit risk scoring model** for new applicants.


## 📜 License

This project is intended for educational and personal use. All rights reserved by **Kashvi1811**.  
*For any usage beyond personal or educational purposes, please contact me in advance.*

## 🤝 Contact & Colloboration

I’m always open to feedback, ideas, and collaboration opportunities! Feel free to reach out:

- **GitHub:** [@Kashvi1811](https://github.com/Kashvi1811)
- **LinkedIn:** https://www.linkedin.com/in/kashvi-soni-6330a92b2/
- **Email:** kashvisoni2005@gmail.com
