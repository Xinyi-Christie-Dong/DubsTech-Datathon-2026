# DubsTech-Datathon-2026

To deepen the analysis, we augmented the 2025 dataset with air quality records from 2020–2024, transforming a single-year snapshot into a six-year longitudinal study.
This expansion serves two key goals:

Stronger Comparisons: Benchmarking 2025 levels against extreme events such as the 2020 wildfire season clarifies long-term trends and signs of atmospheric recovery across California.

Better Forecasting: Multi-year data improves model accuracy by capturing seasonality, climate shocks, and policy impacts, enabling stronger predictions of future median AQI and earlier detection of emerging high-risk hotspots.

# **Access to a Livable Planet**
**Datathon 2026**

**Team:** Bad Bunnies  
**Members:** Anh Do, Christie Dong, Stephanie Balderas, Cannon Hurst

## **Deliverables**
- **Interactive Dashboard (Web):**  
  https://datathon-2026-gamma.vercel.app/#/dashboard

## **Project Overview**
Air pollution poses a major public health risk in the United States, driven by factors such as industrial emissions, transportation density, wildfire activity, and climate change. Using Air Quality Index (AQI) data from 2020 to 2025, this project analyzes spatial patterns in unhealthy air quality and builds a predictive model to support early intervention and resource planning.

Our goal is to combine **descriptive analysis**, **visualization**, and **machine learning** to better understand where air quality risks are most severe and how future conditions can be anticipated.

## **Research Questions**
To keep our analysis focused and actionable, we address the following two questions:

1. **Which states and counties experience the highest number of Unhealthy or Hazardous AQI days?**  
   We analyze historical AQI data to identify geographic hotspots with persistent air quality risks.

2. **Can we predict next year’s number of Unhealthy Days for a county using historical data?**  
   We build and evaluate regression models to forecast unhealthy air quality days and assess their potential use for proactive public health planning.

## **Methodology**
Our workflow follows a clear and reproducible pipeline, with details documented in the accompanying Jupyter notebooks.

### **Data Cleaning and Preparation**
- Aggregated AQI data at the county-year level  
- Handled missing and inconsistent values  
- Engineered key metrics such as the percentage of unhealthy days  
- Standardized features for modeling  

### **Exploratory Data Analysis**
- Identified spatial patterns in unhealthy and hazardous AQI days  
- Compared state-level and county-level trends  
- Highlighted long-term pollution hotspots  

### **Modeling Approach**
- Task type: **Regression**  
- Models tested:
  - Linear Regression (baseline)
  - Random Forest Regressor
- Final model selected: **Random Forest**, due to superior predictive performance

## **Model Performance**
We evaluated models on a held-out test set using standard regression metrics.

### **Baseline Model: Linear Regression**
- R² Score: **55%**
- Mean Absolute Error (MAE): **±1.05 days**

### **Final Model: Random Forest**
- R² Score: **90%**
- Mean Absolute Error (MAE): **±0.29 days**

**Margin of Error Interpretation:**  
On average, the Random Forest model’s predictions differ from the true number of unhealthy days by less than one-third of a day, indicating strong predictive accuracy.

## **Key Findings**
1. **Air pollution risk is concentrated in a few regions.**  
   From 2020 to 2025, air quality issues were not evenly distributed across the U.S. California consistently experienced the highest number of unhealthy air quality days, far exceeding other states. This highlights the influence of regional climate, geography, and pollution sources.

2. **Several California counties remain long-term pollution hotspots.**  
   San Bernardino, Riverside, and Los Angeles counties showed the highest proportions of unhealthy or hazardous days. Although statewide median AQI levels show gradual improvement, these counties continue to face frequent severe pollution events.

3. **Predictive modeling enables early and targeted action.**  
   The Random Forest model, with approximately 90% accuracy, demonstrates strong potential for forecasting unhealthy air quality days. These predictions can support early health warnings, healthcare preparedness, and more efficient allocation of public health resources.
