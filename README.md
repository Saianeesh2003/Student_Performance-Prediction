# Student_Performance-Prediction-Multiple Linear Regression (UCI Dataset)

📘 Project Overview

This project predicts the final student grade (G3) using demographic, family, and academic behavior features.
The goal is to understand which factors influence performance and to build a regression model that generalizes well without data leakage.

I avoided using intermediate grades (G1, G2) as features because they occur after most input variables and artificially boost performance.

🧠 Dataset

Source: UCI Machine Learning Repository

Files: student-mat.csv (Math class)

Rows: 395

Features: 33

Target:

G3 (final grade, 0–20)

🧹 Data Cleaning & Preprocessing

Handled categorical variables using One-Hot Encoding (pd.get_dummies)

Converted boolean dummy columns to integers

Removed G1 and G2 to avoid data leakage

Split dataset into Train (80%) / Test (20%)

📊 Exploratory Data Analysis

Key visualizations include:

Correlation heatmap

Target distribution (G3)

Boxplots (Gender vs G3, Study time vs G3)

Scatterplots (Absences vs G3)

These help understand which features relate most to final performance.

🤖 Modeling
Models Used

Multiple Linear Regression



Evaluation Metrics

R² Score

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

Results
	R² Score	 RMSE
	~0.15	      ~4.4

🔍 Key Findings
Study time, failures, and absences have weak-to-moderate correlation with G3

Alcohol consumption shows slight negative correlation

Gender, internet access, and family support do not strongly impact final grades

Without G1/G2, predicting G3 is challenging (low R² makes sense)
