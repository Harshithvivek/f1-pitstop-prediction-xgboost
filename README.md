# 🏎️ Formula 1 Pit Stop Prediction using XGBoost

## 📌 Project Overview

This project predicts whether a Formula 1 driver will make a pit stop in the next lap using Machine Learning.

The model is trained using race telemetry and tyre-related information such as tyre life, degradation, lap times, race progress, and stint details.

The objective is to build a robust classification model that can assist in race strategy analysis.

---

## 🎯 Problem Statement

Predict:

- 0 → No Pit Stop Next Lap
- 1 → Pit Stop Next Lap

This is a Binary Classification Problem.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Matplotlib
- Jupyter Notebook

---

## 📊 Dataset Features

Some important features include:

- Driver
- Race
- Compound Type
- Tyre Life
- Lap Time
- Race Progress
- Degradation
- Stint Number

Target Variable:

```text
PitNextLap
```

---

## ⚙️ Feature Engineering

Several custom features were created to improve model performance:

### TyreLife_Squared

Captures nonlinear tyre wear patterns.

### TyreLife_Log

Reduces skewness in tyre life values.

### Stint_TyreLife_Interaction

Combines tyre age and stint information.

### RaceProgress_TyreLife

Represents tyre condition throughout race progress.

### Degradation_per_Lap

Measures tyre wear speed.

### LapTime_Degradation

Shows impact of tyre wear on lap times.

### Pit_Urgency

Combines:

```text
TyreLife × Degradation × RaceProgress
```

to estimate pit stop urgency.

---

## 🤖 Machine Learning Pipeline

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Missing Value Handling
5. Encoding Categorical Features
6. Train-Validation Split
7. XGBoost Training
8. ROC-AUC Evaluation
9. Test Predictions
10. Submission Generation

---

## 📈 Model

Algorithm Used:

### XGBoost Classifier

Reasons:

- High performance on tabular data
- Handles nonlinear relationships
- Robust against overfitting
- Excellent feature importance analysis

---

## 📊 Evaluation Metric

ROC-AUC Score

Higher ROC-AUC indicates better discrimination between pit-stop and non-pit-stop scenarios.

---

## 🚀 Results

The model successfully learns race strategy patterns from tyre degradation and race telemetry data and predicts pit stop probability for unseen race situations.

---

## 📂 Repository Structure

```text
├── data
├── notebooks
├── outputs
├── images
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 👨‍💻 Author

Harshith Vivek

B.Tech Computer Science Engineering

Interested in:
- Artificial Intelligence
- Machine Learning
- Data Science
- Generative AI

---

## ⭐ Future Improvements

- Hyperparameter Tuning
- Cross Validation
- LightGBM Comparison
- Ensemble Learning
- Explainable AI using SHAP
