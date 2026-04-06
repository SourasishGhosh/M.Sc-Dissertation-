# M.Sc-Dissertation
M.Sc Dissertation on "A Hybrid Fuzzy–Random Forest Classification Model for SevereWeather Prediction in the Kolkata and North 24 Parganas District Regions"


# Hybrid Fuzzy–Random Forest Model for Severe Weather Prediction

**Author:** Sourasish Ghosh  
**Institution:** University of Calcutta  
**Supervisor:** Prof. Surajit Chattopadhyay  
**Degree:** Master of Science (M.Sc.) in Atmospheric Sciences  
**Year:** 2025

---

## Project Overview

This project presents a **hybrid fuzzy–Random Forest (RF)** model for classifying severe weather events using **24 years of historical meteorological data** (2000–2024) from **Kolkata and North 24 Parganas District Regions** in Eastern India.

The approach integrates **fuzzy logic-based membership matrices** with a **Random Forest classifier**, enabling improved predictions under **uncertainty, skewed data, and overlapping features**.

---

## Data Source

- [Open-Meteo Historical API](https://open-meteo.com/en/docs/historical-weather-api)
- Derived from **ECMWF IFS** (Integrated Forecasting System) **ERRA 5** dataset
- Dataset includes daily records from **March 1, 2000 to March 31, 2024**

### Parameters Used

- Temperature (Mean, Max, Min)
- Relative Humidity
- Wind Speed (10m)
- Precipitation
- Diurnal Temperature Range (DTR)
- Lifting Condensation Level (LCL)
- Wind Gust

---

## Methodology

### 1. **Descriptive Analysis**
- Computed statistical properties (mean, skewness, kurtosis)
- Conducted Chi-squared tests and T-tests to validate feature importance

### 2. **Fuzzy Logic**
- Converted continuous variables into **fuzzy categories** (Low, Medium, High) using quantiles
- Constructed **Binary Fuzzy Relations (BFRs)** via:
  - Max–Min Composition
  - Conditional Probability Matrices

### 3. **Random Forest Classification**
- Fuzzy features were appended to original dataset
- Multi-class RF model trained with **class weighting** to handle imbalanced event data
- Weather events labeled based on **IMD guidelines** and rule-based logic

---

## Results

- **Overall Accuracy**: 88.64%  
- **Macro F1 Score**: 0.87  
- **Best Performing Classes**:  
  -  Humid Heat Wave (F1 ≈ 1.0)  
  -  Cold Wave (F1 ≈ 1.0)  
  -  Tropical Cyclone (F1 ≈ 0.75)

- Misclassifications occurred mainly between **Flood** and **Thunderstorm**, likely due to overlapping features.

---

##  Key Contributions

-  Introduced **fuzzy membership matrices** as interpretable features for weather classification
-  Enhanced machine learning model accuracy with fuzzy-augmented input
-  Addressed **class imbalance** using RF with weighted classes
-  Provided insight into nonlinear interdependencies among meteorological parameters

---

