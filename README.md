# MSCS_634_Lab_1  
**Data Visualization, Data Preprocessing, and Statistical Analysis Using Python**  
**Name:** Bishesh  
**Date:** November 3, 2025  

## Overview
This lab applies data visualization, preprocessing, and statistical analysis techniques to the **Stroke Prediction Dataset** from Kaggle.  
**Data Source:** [Stroke Prediction Dataset – Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

The dataset contains 5,110 records and 12 variables, including demographic, health, and lifestyle factors that may influence stroke occurrence.



## Key Steps
1. **Data Preprocessing**
   - Missing BMI values (201) were imputed with the median.
   - Outliers in *avg_glucose_level* were detected using the IQR method (627 outliers removed).
   - Irrelevant columns (e.g., *id*) dropped and dataset reduced to 3,138 records.
   - Continuous variables (*age, glucose, bmi*) scaled using Min-Max scaling.
   - Age discretized into four categories (*Young, Adult, Middle-Aged, Senior*).

2. **Data Visualization**
   - Scatter plot showed strong interaction between **age** and **average glucose level** in stroke cases.
   - BMI histogram displayed a slightly right-skewed distribution with most individuals in the *overweight* range.

3. **Statistical Analysis**
   - Mean Age = 43 years; Mean BMI = 28.9.
   - Stroke prevalence = 5%.
   - Correlation analysis identified:
     - **Age** (0.23), **Hypertension** (0.12), and **Heart Disease** (0.12) as top predictors.
     - Glucose and BMI showed weak individual correlations with stroke.



## Insights
- **Age** is the most significant risk factor for stroke, followed by **hypertension** and **heart disease**.  
- High glucose levels amplify stroke risk when combined with older age.  
- Dataset shows a strong class imbalance (few stroke cases), requiring resampling for modeling.



## Tools Used
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook  
- Scikit-learn (for scaling)
