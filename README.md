# 🚀 Stock Price Forecasting using LSTM + ARIMA Hybrid Model

## 📌 Overview

This project builds a **hybrid time-series forecasting system** that combines **deep learning (LSTM)** and **statistical modeling (ARIMA)** to predict stock prices with higher accuracy and stability.

Instead of relying on a single model, this approach:
- Uses **LSTM** to capture complex, non-linear patterns in sequential data  
- Uses **ARIMA** to model and correct residual errors  

👉 The outcome is a **robust forecasting pipeline** that reduces prediction bias and improves overall performance.

---

## 🎯 Objective

- Develop an **end-to-end stock forecasting pipeline**
- Improve prediction accuracy using **hybrid modeling**
- Demonstrate **real-world application of AI in financial analytics**

---

## 🧠 Business Impact

This solution reflects how modern organizations leverage **data & AI for growth**:

- 📈 Better financial forecasting  
- 📊 Data-driven investment decisions  
- ⚙️ Reduced model bias and error  
- 🔍 Enhanced trend and pattern detection  

---

## ⚙️ Tech Stack

- **Python**
- **TensorFlow / Keras**
- **Pandas, NumPy**
- **Matplotlib**
- **Statsmodels (ARIMA)**
- **Scikit-learn**

---

## 🏗️ Architecture
Raw Data → Preprocessing → Train/Test Split
↓
LSTM Model
↓
Initial Predictions
↓
Residual (Error) Calculation
↓
ARIMA Model (Errors)
↓
Final Corrected Predictions


---

## 🔄 Workflow

### 1. Data Preprocessing
- Load time-series stock data  
- Handle missing values  
- Structure data for sequential modeling  

---

### 2. Data Transformation
- Convert time-series into supervised learning format  
- Create sequences of past `n` observations  

---

### 3. Train-Test Split
- Chronological split (no random sampling)  
- Maintains time dependency  

---

### 4. LSTM Model
- Captures long-term dependencies in stock prices  
- Learns non-linear relationships  
- Generates initial predictions  

---

### 5. Error Modeling
- Compute residuals: Error = Actual - Predicted


- Identify systematic prediction gaps  

---

### 6. ARIMA Model
- Train ARIMA on residuals  
- Model linear structure in errors  
- Forecast future correction values  

---

### 7. Final Prediction
- Final Prediction = LSTM Prediction + ARIMA Correction
- Produces refined and more accurate outputs  

---

## 📊 Evaluation Metrics

The model is evaluated using:

- **MSE (Mean Squared Error)**  
- **RMSE (Root Mean Squared Error)**  
- **MAE (Mean Absolute Error)**  

These metrics ensure:
- Model accuracy validation  
- Error quantification  
- Performance benchmarking  

---

## 📈 Visualizations

The project generates:

- 📉 Actual vs Predicted Prices  
- 📊 Train vs Test Split  
- ⚠️ Prediction Error Trends  
- 📈 Final Hybrid Predictions  
- 📊 Accuracy Comparison Charts  

---

## 🔍 Key Insights

- LSTM captures **trend and momentum effectively**
- ARIMA improves **precision by correcting residual errors**
- Hybrid model:
  - Reduces overfitting  
  - Handles noise efficiently  
  - Produces smoother predictions  

👉 Combined approach outperforms standalone models in most cases.

---

## 📂 Core Components

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

## 🚀 How to Run

```bash
git clone https://github.com/kevalrakholiya/Stock_Price_Forecasting.git
cd Stock_Price_Forecasting
pip install -r requirements.txt
python main.py
