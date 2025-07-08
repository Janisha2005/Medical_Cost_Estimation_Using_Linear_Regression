# 🏥 Medical Cost Estimation using Linear Regression

> A regression project to predict individual medical charges based on personal, demographic, and lifestyle features using linear regression.

---

## 📌 Project Overview

This project builds a **Linear Regression model** to estimate medical insurance charges using demographic and lifestyle information. The target variable (`charges`) is transformed using the logarithm to handle skewness and improve model performance.

---

## 📂 Dataset

- **Source**: [Kaggle - Medical Cost Personal Dataset](https://www.kaggle.com/mirichoi0218/insurance)
- **Records**: 1338 entries
- **Features**:
  - `age`: Age of the primary beneficiary
  - `sex`: Gender (`male`, `female`)
  - `bmi`: Body mass index
  - `children`: Number of children covered
  - `smoker`: Smoking status (`yes`, `no`)
  - `region`: Residential area in the US
  - `charges`: Medical insurance cost (target)

---

## 📊 Data Preprocessing

- Handled skewness in `charges` using `log(charges)`
- Categorical encoding:
  - `sex` and `smoker` → binary (0/1)
  - `region` → one-hot encoding
- Trained/Test split using `train_test_split()`

---

## 🧠 Model Used

- **Linear Regression** from `sklearn.linear_model`
- Target: `log(charges)`  
- Prediction converted back using `np.exp()` for interpretability

---

## 📈 Model Evaluation

| Metric          | Value (on actual scale) |
|-----------------|--------------------------|
| **MAE**         | \$3,888.77               |
| **RMSE**        | \$7,815.31               |
| **R² Score**    | 0.6066                   |

---

## 📉 Visualizations

- Correlation heatmap
- Boxplots for outlier detection
- Actual vs Predicted line plot

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook
