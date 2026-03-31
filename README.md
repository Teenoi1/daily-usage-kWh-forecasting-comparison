# ⚡ Energy Consumption Forecasting Comparison

This project focuses on **time series forecasting of electricity consumption** using multiple modeling approaches. The goal is to compare the performance of statistical, machine learning, and deep learning models on real-world industrial energy data.

---

## 📌 Project Overview

The dataset contains detailed electricity usage records from **DAEWOO Steel Co., Ltd.** located in Gwangyang, South Korea. The company produces steel coils, steel plates, and iron plates, making energy consumption highly dynamic and critical.

This project compares 3 forecasting approaches:

- 📊 **SARIMA** (Statistical Model)
- 🌲 **XGBoost** (Machine Learning)
- 🧠 **LSTM** (Deep Learning)

---

## 📂 Dataset

This project uses the **Steel Industry Energy Consumption Dataset** from Kaggle:

🔗 https://www.kaggle.com/datasets/haideradnan77/steel-industry-energy-consumption-daewoo-steel-co

### 📊 Description

The dataset contains high-resolution electricity consumption data collected from **DAEWOO Steel Co., Ltd.** in Gwangyang, South Korea.

- Covers industrial energy usage over time  
- Includes electrical measurements and operational indicators  
- Suitable for time series forecasting and machine learning tasks  

📌 The data was collected via a cloud-based system and synchronized with the Korea Electric Power Corporation (KEPCO) :contentReference[oaicite:0]{index=0}  

---

### 🧩 Features

- `Usage_kWh` → Energy consumption (target variable)  
- `Lagging_Current_Reactive.Power_kVarh`  
- `Leading_Current_Reactive_Power_kVarh`  
- `CO2(tCO2)`  
- `Lagging_Current_Power_Factor`  
- `Leading_Current_Power_Factor`  
- `NSM` (Number of seconds from midnight)  
- `WeekStatus` (Weekday / Weekend)  
- `Day_of_week`  
- `Load_Type` (Light / Medium / Maximum)  

---

### 📈 Dataset Characteristics

- ⏱️ High-frequency time series (~35,000 records) :contentReference[oaicite:1]{index=1}  
- 🔁 Strong seasonal patterns (weekly cycles)  
- ⚡ Real industrial energy consumption behavior  
- 🏭 Reflects operational load conditions  

---

### 📌 Use Cases

- Energy consumption forecasting  
- Peak demand prediction  
- Industrial optimization  
- Machine learning & time series modeling  


- **Type:** Time Series  
- **Target:** `Usage_kWh`  
- **Frequency:** High-resolution (later resampled for efficiency)  

### Characteristics:
- Strong **seasonality (weekly patterns)**  
- Trend + Noise components  
- Industrial-scale energy consumption  

---

## 🔍 Exploratory Data Analysis (EDA)

Key steps:

- Time series visualization  
- Decomposition into:
  - Observed  
  - Trend  
  - Seasonal  
  - Residual  

### 📌 Insight:
- Clear **weekly seasonal pattern**  
- Suitable for both statistical and learning-based models  

---

## ⚙️ Methodology

### 📊 SARIMA (Statistical Approach)

- Handles trend and seasonality explicitly  
- Seasonal period initially set to `s = 96`  
- Optimized by resampling to reduce computation cost  

---

### 🌲 XGBoost (Machine Learning)

- Converts time series into supervised learning problem  
- Uses:
  - Lag features  
  - Feature engineering  

**Strength:**
- Handles non-linear relationships well  

---

### 🧠 LSTM (Deep Learning)

- Designed for sequential data  
- Captures long-term dependencies  

**Requires:**
- Data normalization  
- Sequence windowing  

📌 **Tip:** Use validation split to prevent overfitting  

---

## 📏 Evaluation Metrics

Models are evaluated using:

- **MAE** (Mean Absolute Error)  
- **RMSE** (Root Mean SquARED Error)  
- **MAPE** (Mean Absolute Percentage Error)  

---

## 📊 Results

| Model    | Performance |
|----------|------------|
| SARIMA   | Baseline   |
| LSTM     | Moderate   |
| XGBoost  | ⭐ Best    |

🏆 **XGBoost achieved the best performance across all metrics**

Example:
- MAE ≈ **1.73** (lowest error)

---

## 🧠 Key Insights

- Traditional models (SARIMA) struggle with complex patterns  
- LSTM performs well but requires careful tuning  
- **XGBoost is the most effective for this dataset**  
