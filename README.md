# Stock Price Forecasting using LSTM + ARIMA Hybrid Model

## Overview

This project focuses on building a stock price forecasting system using a hybrid approach that combines LSTM (Long Short-Term Memory) and ARIMA models.

Instead of relying on a single method, the model uses LSTM to learn patterns from historical data and ARIMA to correct prediction errors. This helps improve overall accuracy and stability in forecasts.

---

## Objective

- Build a complete time-series forecasting pipeline  
- Improve prediction performance using a hybrid modeling approach  
- Apply machine learning and statistical methods to a real-world financial use case  

---

## Approach

The model works in two stages:

- LSTM captures trends, seasonality, and non-linear patterns in stock prices  
- ARIMA is applied on residual errors to correct consistent deviations  

Final prediction is calculated by combining both outputs: Final Prediction = LSTM Prediction + ARIMA Correction

---

## Tech Stack

- Python  
- TensorFlow / Keras  
- Pandas, NumPy  
- Matplotlib  
- Statsmodels (ARIMA)  
- Scikit-learn  

---

## Architecture
Raw Data → Preprocessing → Train/Test Split
→ LSTM Model → Initial Predictions
→ Residual Calculation
→ ARIMA Model (on errors)
→ Final Predictions

---

## Workflow

### 1. Data Preprocessing
- Load stock price data  
- Handle missing values  
- Prepare data for time-series modeling  

### 2. Data Transformation
- Convert time-series into supervised learning format  
- Create sequences using past observations  

### 3. Train-Test Split
- Use chronological split  
- Preserve time dependency (no random sampling)  

### 4. LSTM Model
- Train model on sequential data  
- Capture long-term dependencies and non-linear patterns  
- Generate initial predictions  

### 5. Residual Analysis
- Calculate prediction errors  
- Identify patterns in residuals  

### 6. ARIMA Model
- Train ARIMA on residuals  
- Model linear structure in errors  
- Generate correction values  

### 7. Final Output
- Combine LSTM predictions with ARIMA corrections  
- Produce refined forecasts  

---

## Evaluation Metrics

- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  
- Mean Absolute Error (MAE)  

These metrics are used to measure accuracy and compare model performance.

---

## Visualizations

- Actual vs Predicted Prices  
- Train vs Test Split  
- Prediction Error Trends  
- Final Hybrid Model Output  
- Accuracy Comparison  

---

## Key Observations

- LSTM performs well in capturing overall trends  
- ARIMA helps correct systematic errors  
- Hybrid model produces more stable predictions  
- Works better than using LSTM or ARIMA alone in most cases  

---

## Project Structure

### Data Processing
- `data_loader()`  
- `data_allocation()`  

### Transformation
- `apply_transform()`  

### Modeling
- `LSTM()`  
- `ARIMA_Model()`  

### Evaluation
- `calculate_accuracy()`  
- `Error_Evaluation()`  

### Visualization
- `plot_predictions()`  
- `plot_final_predictions()`  
- `plot_accuracy()`  

---

## How to Run

```bash
git clone https://github.com/kevalrakholiya/Stock_Price_Forecasting.git
cd Stock_Price_Forecasting
