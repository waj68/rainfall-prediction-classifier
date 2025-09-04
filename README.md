# 🌧️ Rainfall Prediction Classifier

## 📌 Project Overview
This project builds a machine learning classifier to predict rainfall using historical weather data from the **Australian Bureau of Meteorology** (2008–2017). The analysis focuses on Melbourne and nearby locations, applying feature engineering and supervised learning to estimate the probability of rain.

## 🗂️ Dataset
- Source: [Bureau of Meteorology](http://www.bom.gov.au/climate/dwo/) & [Kaggle Weather Dataset](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package/)
- Records: ~56,000 daily weather observations
- Selected subset: ~7,500 observations from Melbourne, Melbourne Airport, and Watsonia
- Target: `RainToday` (Yes/No)

## 🔧 Methods & Workflow
1. **Preprocessing**
   - Dropped rows with missing values
   - Stratified train-test split (80/20)
   - Categorical encoding with `OneHotEncoder`
   - Feature scaling for numeric features

2. **Feature Engineering**
   - Created `Season` variable from `Date`
   - Considered location-specific granularity

3. **Modeling**
   - **Random Forest Classifier** (pipeline with preprocessing)
   - GridSearchCV hyperparameter tuning (`n_estimators`, `max_depth`, `min_samples_split`)
   - Compared with **Logistic Regression** baseline

4. **Evaluation**
   - Accuracy, Precision, Recall, F1-score
   - Confusion Matrix
   - Feature Importance visualization

## 📊 Results
- **Best Model:** Random Forest  
- **Cross-validation Accuracy:** 0.85  
- **Test Set Accuracy:** 0.84  
- **Performance by Class:**  
  - "No Rain" → Precision 0.86, Recall 0.95  
  - "Rain" → Precision 0.75, Recall 0.51  

Confusion Matrix:  
![Confusion Matrix](images/confusion_matrix.png)

Top 20 Feature Importances:  
![Feature Importances](images/feature_importances.png)

## 🌍 Applications
- Short-term weather predictions
- Risk assessment for agriculture, commuting, and event planning
- Example workflow for other **binary classification tasks** in health, climate, and social sciences

## 🛠️ Tools & Libraries
- Python, pandas, NumPy, scikit-learn, seaborn, matplotlib

## 📂 Repository Structure
- `notebook.ipynb` → full workflow  
- `images/` → figures (confusion matrix, feature importances)  
- `README.md` → project summary (this file)  

---

