# Credit Risk Modeling – Part 1: Data Processing and Feature Engineering

## 📌 Project Description

This repository contains the first phase of a credit risk modeling project using the Lending Club loan dataset. The goal of this stage is to prepare clean, structured, and predictive features to be used in later model development. It includes comprehensive data cleaning, missing value handling, multicollinearity reduction, and advanced feature engineering (e.g., Weight of Evidence, IV analysis).

📊 Dataset
We use the publicly available [Lending Club Loan Data (Kaggle)](https://www.kaggle.com/datasets/wendykan/lending-club-loan-data). It contains over 2.2 million accepted loan applications from 2007 to Q4 2018. The dataset includes a rich set of features such as loan amount, interest rate, income, employment length, credit history, and loan status.

The data is divided into two periods:

- **Development set** (2007 to 2015): used for training and validation.
- **Out-of-time test set** (2016 to 2018): used for evaluating the model’s generalization.

## 🧰 Features & Workflow

### ✅ 1. Data Loading
- Import large `.csv` files from Kaggle
- Combine or subset datasets by period

### ✅ 2. Missing Value Treatment
- Drop features with excessive missing values (> 30%)
- Impute remaining missing values with statistical or rule-based methods

### ✅ 3. Target Variable Construction
- Define `default` as target (charged-off, default, late loans marked as 1)

### ✅ 4. Data Splitting
- Divide data into training and test sets based on time periods

### ✅ 5. Categorical Feature Processing
- Convert nominal and ordinal variables using:
  - Label Encoding (if few categories)
  - WoE Binning based on Information Value (IV) analysis

### ✅ 6. Continuous Feature Engineering
- Drop multicollinear features using Variance Inflation Factor (VIF) analysis
- Perform binning and transformation (quantiles, WoE encoding)

### ✅ 7. Final Dataset
- Export processed datasets in `.csv` for modeling
