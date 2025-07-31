# Edunet-Skills4future-Artifical-Intelligence-Internship
This repo will contain weekly as well as final project submission on EV Vehicle/Charging Demand Prediction project completed under Edunet Internship 

# 🚗 EV Adoption Forecasting

This project focuses on forecasting electric vehicle (EV) adoption trends using historical vehicle registration data from Washington State. The predictions help in understanding and preparing for future infrastructure needs, especially EV charging stations.

---

## 📌 Problem Statement

As EV adoption increases rapidly, urban planners need accurate forecasts to plan for supporting infrastructure like charging stations. Poor planning can result in congestion, user dissatisfaction, and missed sustainability goals.

**Objective:**  
Build a machine learning model to predict the number of electric vehicles in the future based on trends in historical data.

---

## 📊 Dataset

The dataset contains monthly EV registration data from the Washington State Department of Licensing, spanning from **January 2017 to February 2024**.  
It includes:

- Date of registration  
- County and state  
- Vehicle type: Battery Electric Vehicles (BEVs), Plug-In Hybrid Electric Vehicles (PHEVs)  
- Total number of electric and non-electric vehicles  
- Percent of EVs in total vehicles  

---

## 🧠 Solution Approach

- **Model Used:** Random Forest Regressor  
- **Hyperparameter Tuning:** Performed using `RandomizedSearchCV`  
- **Best Parameters:**
  - `n_estimators`: 200  
  - `max_depth`: 15  
  - `min_samples_split`: 4  
  - `min_samples_leaf`: 1  
  - `max_features`: None  

### ✅ Model Evaluation
- **Mean Absolute Error (MAE):** 0.01  
- **Root Mean Squared Error (RMSE):** 0.06  
- **R² Score:** 1.00  

The model showed excellent performance in learning patterns from the historical data and predicting future EV adoption accurately.

---

## 🚀 Deployment

The project is deployed using **Streamlit** for interactive visualization.

### 📈 Features Available:

1. **Single County Forecast:**  
   View a line plot showing predicted EV adoption for the next 3 years for any selected county.

2. **Multi-County Comparison:**  
   Compare EV adoption trends between **any 3 counties** using a line chart with 3 distinct lines.

---

## 🔍 Future Scope

- Add more data sources (e.g., energy usage, fuel prices, weather conditions)
- Try advanced models like LSTM for deeper time-series forecasting
- Extend to other states or countries for a wider impact

---

## 🛠️ Tech Stack

- **Python** – Core programming language  
- **Pandas, NumPy** – Data manipulation  
- **Matplotlib, Seaborn** – Data visualization  
- **Scikit-learn** – Machine Learning models  
- **Streamlit** – Web app deployment  
- **Joblib** – Model serialization  

---

## 📂 How to Run Locally

```bash
git clone https://github.com/yourusername/ev-adoption-forecasting.git
cd ev-adoption-forecasting
pip install -r requirements.txt
streamlit run app.py

