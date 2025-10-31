# 🧠 Health Score Prediction using Machine Learning  

### Predicting an individual’s health score based on lifestyle and physiological factors  

---

## 📋 Project Overview  

This project focuses on **predicting a synthetic health score** using various **machine learning regression algorithms**.  
The dataset includes features such as **Age**, **BMI**, **Exercise Frequency**, **Diet Quality**, **Sleep Hours**, **Smoking Status**, and **Alcohol Consumption**, which all contribute to the overall **Health Score**.  

The workflow includes **data exploration**, **preprocessing**, **model training**, **cross-validation**, **hyperparameter tuning**, and **model evaluation**.

---

## 🧰 Tech Stack  

| Category | Tools / Libraries |
|-----------|-------------------|
| **Language** | Python 3 |
| **Data Handling** | pandas, numpy |
| **Visualization** | matplotlib, seaborn |
| **Modeling** | scikit-learn |
| **Model Saving** | pickle |
| **Warnings Management** | warnings |

---

---

## 🧠 Problem Statement  

The goal is to build a **regression model** that predicts an individual's **health score** based on their lifestyle and health indicators.  
Since the target variable is continuous, this is a **supervised regression task**.

---

## 🔍 Workflow  
---
Health-Score-Prediction/
│
├── notebook.ipynb # Original Jupyter notebook
├── health_score_prediction.py # Converted Python script
├── synthetic_health_data.csv # Dataset used in the analysis
├── best_model.pkl # Saved trained model
└── README.md # Project documentation

---

### 1. **Data Loading**
- Loaded the dataset using `pandas`.
- Checked for missing values and duplicates.
- Data was already clean — no preprocessing needed.

### 2. **Exploratory Data Analysis (EDA)**
- Conducted **univariate** and **bivariate** analysis using visualizations.
- Generated **correlation heatmaps** to identify strong relationships.

**Key Insights:**
- Most features are normally distributed.
- `Health_Score` was skewed → applied log transformation.
- Strong correlations found between **BMI**, **Diet Quality**, and **Sleep Hours** with the target.

### 3. **Data Preprocessing**
- Handled outliers using the **IQR method**.
- Applied `np.log1p()` to normalize the target variable.
- Split dataset into **train (80%)** and **test (20%)** sets.

### 4. **Model Training**
Trained multiple baseline regression models:
- Linear Regression  
- Ridge & Lasso Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- Support Vector Regressor (SVR)  
- K-Nearest Neighbors  

### 5. **Model Evaluation**
Evaluated models using:
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

**Best Baseline Model:** Gradient Boosting Regressor  

### 6. **Cross-Validation & Hyperparameter Tuning**
Performed **5-Fold Cross-Validation** and **Grid Search** for:
- Gradient Boosting  
- Random Forest  
- SVR  

**Final Best Model:** Support Vector Regressor (SVR)  

### 7. **Final Model Evaluation**
| Metric | Train Set | Test Set |
|:-------|:-----------|:----------|
| R² | High | High |
| MAE | Low | Low |
| RMSE | Low | Low |

*(Exact scores will be displayed when the script is executed.)*

### 8. **Model Saving**
The final SVR model was saved for deployment:
```python
with open("best_model.pkl", "wb") as f:
    pickle.dump(best_model, f)
```
```
git clone https://github.com/<your-username>/Health-Score-Prediction.git
cd Health-Score-Prediction
```
## Author 
## Rahma Saber Abbas

## 📂 Project Structure  

