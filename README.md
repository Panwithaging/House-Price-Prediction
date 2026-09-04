## House Price Prediction using Machine Learning

## Overview

This project predicts residential property prices using multiple Machine Learning regression algorithms. The complete workflow includes data cleaning, exploratory data analysis (EDA), feature engineering, preprocessing, model comparison, hyperparameter tuning, and final prediction generation.

The objective was to build a regression model capable of accurately predicting house prices based on property characteristics such as square footage, number of bedrooms, location, builder information, and geographical coordinates.

---

## Dataset

**Source:**
https://www.kaggle.com/datasets/anmolkumar/house-price-prediction-challenge/data

### Features

- POSTED_BY
- UNDER_CONSTRUCTION
- RERA
- BHK_NO.
- BHK_OR_RK
- SQUARE_FT
- READY_TO_MOVE
- RESALE
- ADDRESS
- LONGITUDE
- LATITUDE

**Target Variable**

- TARGET(PRICE_IN_LACS)

---

## Project Workflow

### 1. Data Exploration
- Loaded training and testing datasets
- Checked dataset shape
- Inspected data types
- Summary statistics
- Missing value analysis

### 2. Exploratory Data Analysis (EDA)

Visualizations were created to understand the relationship between important variables.

Examples include:

- Square Foot vs Price
- BHK vs Price
- Posted By vs Price
- BHK/RK vs Price

Histograms, Scatter Plots and Box Plots were used to identify distributions and possible outliers.

---

### 3. Data Cleaning

- Checked for missing values
- Checked duplicate records
- Investigated extreme observations
- Cleaned categorical values

Some observations appeared unusual but were **not removed** because there was insufficient evidence that they were incorrect records.

The **test dataset was not modified by removing rows**, since every observation requires a prediction for the final submission.

---

### 4. Feature Engineering

Created additional features to improve model performance.

Examples:

- Extracted **CITY** from ADDRESS
- Created **BHK_PER_SQ_FT**

---

### 5. Data Preprocessing

- Log Transformation (`log1p`) for skewed features
- One-Hot Encoding for categorical variables
- Standard Scaling for numerical variables
- ColumnTransformer
- Pipeline

---

## Machine Learning Models

The following regression models were trained and compared:

- Linear Regression
- K-Nearest Neighbors Regressor
- Decision Tree Regressor
- Random Forest Regressor

---

## Hyperparameter Tuning

The best-performing model (Random Forest Regressor) was further optimized using **GridSearchCV**.

---

## Model Performance

### Final Model
**Random Forest Regressor (GridSearchCV)**

| Metric | Value |
|--------|-------:|
| Cross Validation Score | **85%** |
| MAE | **28.25** |
| RMSE | **124.23** |
| R² Score | **0.9527** |

The tuned Random Forest model achieved the best overall performance and was selected as the final model.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Repository Structure

```
House-Price-Prediction/
│
├── House_Price_research.ipynb
├── README.md
├── requirements.txt
├── submission.csv
```

---

## How to Run

1. Clone this repository

```bash
git clone <repository-url>
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Open the notebook

```bash
jupyter notebook
```

or open the notebook directly using VS Code.

---

## Future Improvements

- Experiment with XGBoost, LightGBM and CatBoost
- Perform more advanced feature engineering
- Explore feature importance techniques
- Investigate SHAP for model explainability
- Try additional hyperparameter optimization methods

---

## Author

**Tushar Panging**

Machine Learning | Data Analytics | Python