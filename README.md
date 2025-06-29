# 📈 Google Stock Price Prediction using Machine Learning

This project explores and compares the performance of multiple machine learning models—**LSTM**, **Random Forest**, **XGBoost**, and **Support Vector Regression (SVR)**—to predict the next 10 days of **Google’s adjusted closing stock prices**. It was submitted as part of the *Algorithmic Trading (INT424)* course in the **M.Sc. Data Science** program at **SASTRA Deemed University**.

## 🧠 Models Used

- **LSTM (Long Short-Term Memory)**: Recurrent neural network suitable for sequential data.
- **Random Forest**: Tree-based ensemble model.
- **XGBoost**: Boosting technique that improves model accuracy and performance.
- **SVR (Support Vector Regression)**: Kernel-based model for capturing complex nonlinear patterns.

## 🎯 Project Objective

To forecast the **adjusted closing price of Google stock** for the next 10 business days using historical data and compare the predictive performance of various ML models.

## 📊 Evaluation Metrics

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score (Coefficient of Determination)**

### 📋 Model Performance Summary

| Model         | MAE     | RMSE    | R² Score |
|---------------|---------|---------|----------|
| LSTM          | 0.0108  | 0.0141  | 0.9964   |
| Random Forest | 0.0034  | 0.0062  | 0.9993   |
| XGBoost       | 0.0034  | 0.0062  | 0.9993   |
| SVR           | 0.8700  | 1.2900  | 0.9992   |

## 📌 Key Findings

- **Random Forest** and **XGBoost** demonstrated superior performance with minimal prediction errors and near-perfect fit.
- **LSTM** effectively captured time-dependent behavior but had slightly higher error rates.
- **SVR**, despite its high R² score, had large prediction errors, indicating lower reliability.

## 🗃 Dataset Information

- **Source**: [Kaggle – Google Stock Data 2024](https://www.kaggle.com/)
- **Period**: August 2004 – December 2024
- **Features**:
  - `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`

## ⚙️ Data Preprocessing

- Checked and filled missing values
- Converted `Date` to datetime and set as index
- Normalized `Adj Close` column using MinMaxScaler
- Created 30-day sliding windows for sequence modeling

## 📈 Forecasting Strategy

Each model was trained using the past 30 days of `Adj Close` data to forecast the next 10 business days. The predictions were compared against real values using graphs and evaluation metrics.

## 🧰 Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow/Keras
- XGBoost
- Matplotlib, Seaborn

## 🔍 Visualizations

- Individual line plots of predicted vs. actual prices for each model
- Combined comparison plot of all 4 models + real stock prices

## 🚀 Future Work

- Incorporate external features like macroeconomic indicators, news sentiment, or social media signals
- Build hybrid models (e.g., LSTM + XGBoost) or attention-based networks
- Test models across different stocks and markets
- Implement real-time learning systems for live trading environments

## 👨‍🎓 Author

**Gobikrishnan V.S**  
M.Sc. Data Science  
SASTRA Deemed University  

---

