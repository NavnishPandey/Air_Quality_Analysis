# 🌍 Air Quality Analysis for Research and Data Mining

## 📌 Project Overview
This project performs an **in-depth exploratory analysis and predictive modeling of urban air quality** using the **Air Quality UCI Dataset**.  
The dataset contains **ground-truth pollution measurements**, **low-cost sensor responses**, and **meteorological variables** recorded hourly over more than one year.

The goal of the project is to **understand pollution behavior**, **evaluate environmental drivers**, and **build predictive models** that can support **research, policy-making, and intelligent monitoring systems**.

---

## 🎯 Purpose of the Project

The primary objectives of this project are:

1. **Understand Urban Air Pollution Patterns**
   - Identify daily and seasonal pollution trends
   - Detect peak pollution hours in urban environments

2. **Study Environmental Effects**
   - Analyze how **temperature**, **relative humidity**, and **absolute humidity** affect pollutant concentrations

3. **Model Pollution Dynamics**
   - Predict next-hour air quality using:
     - Naive baseline models
     - Machine learning (Random Forest)
     - Time-series models (ARIMA)

4. **Translate Pollution to Health Impact**
   - Convert pollutant concentrations into **Air Quality Index (AQI) categories**
   - Quantify unhealthy exposure duration

5. **Analyze Pollutant Interactions**
   - Use **time-lagged cross-correlation** to understand how pollutants co-evolve

---

## 📂 Dataset Description

**Source:** Air Quality UCI Repository  
**Time Resolution:** Hourly  
**Total Records:** 9,358 hours  

### Ground Truth Pollutants
- CO (Carbon Monoxide)
- NOx (Nitrogen Oxides)
- NO₂
- Benzene (C₆H₆)
- Total Hydrocarbons

### Low-Cost Sensor Signals
- Metal Oxide (MOX) sensor responses
- Used to infer gas behavior (not direct concentrations)

### Meteorological Variables
- Temperature (°C)
- Relative Humidity (%)
- Absolute Humidity (g/m³)

---

## 🔬 Research Questions Addressed

### 1️⃣ Effect of Temperature & Humidity on Pollution
- Linear regression showed **weak relationships**, especially for CO
- NOx decreases with higher temperatures due to better dispersion
- Non-linear models (Random Forest) improved performance slightly

---

### 2️⃣ Peak Hours of Pollution
- **7 PM (19:00)** identified as the peak hour for:
  - CO
  - NOx
  - NO₂
  - Benzene
- Strongly linked to **evening traffic rush hours**

---

### 3️⃣ Next-Hour Air Quality Prediction
Models evaluated:
- **Naive Persistence Model**
- **Random Forest with Lag Features**
- **ARIMA Time-Series Model**

📊 **Best Model: Random Forest with lagged features**
- R² ≈ **0.70**
- MAE ≈ **0.5**
- Clearly outperformed baseline and ARIMA

---

### 4️⃣ Air Quality Index (AQI) Classification
- Pollution levels translated into AQI categories:
  - Good
  - Moderate
  - Unhealthy for Sensitive Groups
  - Unhealthy
  - Very Unhealthy
  - Hazardous

📌 Key findings:
- **56.7% of hours** had unhealthy air quality
- Frequent risk to children, elderly, and respiratory patients
- Seasonal and monthly variability observed

---

### 5️⃣ Time-Lagged Cross-Correlation Between Pollutants
- Strong positive correlations between pollutants
- All major pollutants peak **simultaneously (zero lag)**
- Indicates **common emission sources** (traffic, combustion)

---

### 6️⃣ Absolute Humidity Impact on Pollutant Dispersion
- Higher absolute humidity:
  - Reduces **NOx** and **NO₂**
  - Slightly increases **CO**
  - Increases **Benzene**
- Statistical tests confirm **significant differences**

---

## 🧠 Methods & Techniques Used

- Data cleaning & missing value handling
- Correlation and regression analysis
- Random Forest regression
- ARIMA time-series modeling
- Lag feature engineering
- AQI rule-based classification
- Cross-correlation analysis
- Statistical hypothesis testing (t-tests)

---

## 🛠️ Technologies & Libraries

- **Python**
- Pandas, NumPy
- Scikit-learn
- Statsmodels
- Matplotlib, Seaborn
- SciPy

---

## 🌱 Impact of the Project

### 🔬 Research Impact
- Provides a **comprehensive benchmark analysis** for air quality modeling
- Demonstrates strengths and limitations of ML vs time-series methods
- Useful for environmental and atmospheric research

### 🏙️ Societal Impact
- Highlights **persistent urban air quality risks**
- Identifies **high-risk hours** for public exposure
- Supports data-driven pollution mitigation strategies

### 🤖 Technological Impact
- Shows how **low-cost sensors + ML** can estimate real pollution
- Enables short-term air quality forecasting
- Can be extended to smart city and IoT monitoring systems

### 🏥 Health & Policy Impact
- AQI-based insights help communicate risk clearly to the public
- Supports early warnings for sensitive populations
- Useful for urban planning and traffic regulation policies

---

## 🚀 Future Extensions

- Multi-step forecasting (6–24 hours ahead)
- LSTM / Transformer-based time-series models
- Spatial analysis using multiple monitoring stations
- Sensor calibration using ground truth models
- Real-time dashboard deployment

---

## 📜 Conclusion

This project demonstrates how **data science and machine learning** can transform raw environmental data into **actionable insights**.  
It bridges the gap between **sensor data**, **pollution science**, and **public health**, making it valuable for **research, smart cities, and environmental policy**.

---
