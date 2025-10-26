# Weather Data Prediction

This project implements a **machine learning–based temperature forecasting model** using **global historical weather data (1750–2015)**.  
The model predicts **Land and Ocean Average Temperature** based on related land temperature indicators.

---

## Requirements
[pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  
jupyter]

---

## Overview
The notebook demonstrates a complete workflow for temperature prediction using environmental data:

- Data loading and inspection  
- Cleaning and feature selection  
- Correlation analysis and visualization  
- Regression model training and testing  
- Error evaluation (RMSE) and model validation  

---

## Dataset
**Source:** Berkeley Earth / Kaggle – *Global Land and Ocean Temperature Dataset*  
**Records:** 3,192 monthly observations (1750–2015)  
**Columns:**
- `LandAverageTemperature`
- `LandMaxTemperature`
- `LandMinTemperature`
- `LandAndOceanAverageTemperature`
- Associated uncertainty measures (removed during preprocessing)

**Target variable:**  
`LandAndOceanAverageTemperature` (global mean surface temperature)

---

## Key Concepts

- **Data Cleaning:** Handling nulls, dropping uncertainty fields, resetting date index.  
- **Feature Correlation:** Strong relationships observed among land temperature metrics (r ≈ 0.99).  
- **Feature Selection:** Statistical ranking using `SelectKBest`.  
- **Regression Modeling:** Random Forest Regressor with standardization pipeline.  
- **Model Evaluation:** Root Mean Squared Error (RMSE) for quantitative accuracy.

---

## Run Locally
```bash
> clone repository

pip install -r requirements.txt
jupyter notebook weather_data_prediction.ipynb
```

Ensure weather_data.csv is located in the same directory before running.

---

## Results
RMSE ≈ 0.04 on training data

RMSE ≈ 0.05 on test data

Model demonstrates robust performance and minimal overfitting.

Correlation matrix indicates high linear dependence among temperature variables.

---
## Visualizations

Data Correlation Heatmap

<img width="600" height="243" alt="Image" src="https://github.com/user-attachments/assets/02e30de2-4ef9-4ab0-a8c9-9572150cabdb" />

Model Pipeline and Output

<img width="500" height="400" alt="Image" src="https://github.com/user-attachments/assets/0d3266cc-2a8e-45c6-90a8-bc61f7bb5af3" />

---

## Notes
This project is a demonstration of applying regression methods to weather data for academic purposes, no where is it production grade. 
