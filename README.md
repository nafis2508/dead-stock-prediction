````markdown
# Dead Stock Prediction

## Overview

This project applies predictive analytics and machine learning to identify inventory items at risk of becoming dead stock. Dead stock refers to items that remain unused, unsold, or unmoved for a long period, creating unnecessary storage cost and tying up working capital.

The analysis was conducted on a real-world inventory dataset from a manufacturing and retail context. The objective was to clean, prepare, model, and interpret inventory data to support better stock control and business decision making.

> Note: The original dataset is excluded from this repository due to privacy and confidentiality considerations.

---

## Business Problem

Inventory-heavy businesses often hold stock that no longer contributes to sales or operations. These items increase storage costs, reduce warehouse efficiency, and limit cash flow.

This project aims to answer:

- Which inventory items are likely to become dead stock?
- Which inventory features are most useful for prediction?
- Can machine learning support better inventory decision making?
- Which model performs better for dead stock classification?

---

## Project Objectives

- Clean and prepare inventory data for modelling
- Handle categorical and numerical variables
- Encode warehouse, state, item type, base unit, business area, and ABC class features
- Build train and test datasets for classification
- Train Logistic Regression and Random Forest models
- Compare model performance
- Interpret key drivers of dead stock risk

---

## Dataset Summary

The dataset includes 3,000 inventory records with features related to:

- Inventory quantity
- Unit cost
- Inventory value
- Inventory ageing
- Monthly demand
- Warehouse location
- State
- ABC class
- Business area
- Item type
- Inventory turnover
- Dead stock status

The target variable is:

```text
Dead stock
````

---

## Methodology

### 1. Data Cleaning

The project includes:

* Removing identifier columns
* Removing long free-text item descriptions
* Checking missing values
* Preparing numerical and categorical variables
* Validating feature types

### 2. Feature Engineering

Categorical variables were transformed using encoding techniques, including:

* State dummy variable encoding
* Warehouse dummy variable encoding
* Item type grouping
* Base unit encoding
* Business area encoding
* ABC class encoding

Item types were grouped into:

* Finished Goods
* Raw Materials
* WIP Manufactured
* Other

### 3. Model Preparation

The modelling workflow included:

* Creating feature matrix `X`
* Creating target array `y`
* 80/20 train-test split
* Stratified sampling
* Standardisation using `StandardScaler`

### 4. Machine Learning Models

Two classification models were trained:

* Logistic Regression
* Random Forest Classifier

Model performance was evaluated using training and test accuracy.

---

## Model Results

### Logistic Regression

Logistic Regression achieved strong and stable performance, with both training and test accuracy around 99.5%. This suggests the dataset contains strong predictive signals and may be close to linearly separable.

### Random Forest

Random Forest achieved very high performance, with training accuracy reaching 100% and test accuracy ranging between approximately 99.79% and 100%, depending on model settings.

### Recommended Model

Random Forest is recommended because it performed slightly better and can capture nonlinear relationships between inventory behaviour, stock ageing, turnover, and dead stock risk.

---

## Key Business Insights

* Inventory ageing and slow movement indicators are likely strong predictors of dead stock.
* Warehouse and item type information can help identify operational patterns in stock accumulation.
* Random Forest provides strong predictive performance for classification.
* Predictive analytics can help inventory teams flag dead stock risk earlier and reduce unnecessary holding costs.
* The model can support better purchasing, stock review, warehouse planning, and inventory optimisation decisions.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Logistic Regression
* Random Forest
* StandardScaler
* Jupyter Notebook

---

## Repository Structure

```bash
dead-stock-prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── DeadStockPrediction.ipynb
│
├── reports/
│
├── visuals/
│
├── README.md
└── .gitignore
```

---

## Privacy Note

The original inventory dataset is not included in this repository because it contains real-world operational data. The repository focuses on the analytics workflow, modelling approach, and business interpretation.

---

## Future Improvements

Potential future enhancements include:

* Add confusion matrix and classification report
* Include feature importance visualisation
* Build an interactive inventory risk dashboard
* Add probability-based dead stock risk scoring
* Compare additional models such as XGBoost and Gradient Boosting
* Create a reusable prediction pipeline for new inventory data

---

## Author

**Muntasir Md Nafis**
Master of Business Analytics
Macquarie University
Sydney, Australia

````

