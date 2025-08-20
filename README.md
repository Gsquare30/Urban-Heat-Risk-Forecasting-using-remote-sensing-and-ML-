📌 Overview

This project focuses on urban heat risk assessment and forecasting for Ranchi, India. Using a combination of remote sensing data (MODIS, Sentinel-2 NDVI), climate datasets (NASA POWER), and machine learning models (Random Forest, ARIMA, LSTM), the study identifies high-risk zones and forecasts potential extreme heat periods affecting vulnerable populations.
🚀 Features
✅ Vegetation analysis with Sentinel-2 NDVI

✅ Climate parameter integration (temperature, humidity, rainfall) from NASA POWER API

✅ Machine Learning Models for risk classification

Random Forest (classification of risk categories)

ARIMA (time-series temperature forecasting)

LSTM (deep learning–based risk forecasting)

✅ Visualization of urban heat risk trends & hotspots

🛠️ Tech Stack

Programming Language: Python

Libraries:

Remote Sensing: geemap, earthengine-api, rasterio, shapely, osmnx

Data Handling: pandas, numpy, geopandas

Machine Learning: scikit-learn, xgboost, tensorflow, statsmodels

Visualization: matplotlib, seaborn, plotly, folium

Data Sources:

Sentinel-2 NDVI

NASA POWER Climate Data

🔑 Methodology

The workflow of this project can be divided into five main stages:

1️⃣ Data Acquisition

Sentinel-2 NDVI: Extracted vegetation indices for assessing green cover and its cooling effects.

NASA POWER Climate Data: Collected temperature, relative humidity, and precipitation values through API calls.

OSM Data: Extracted city boundaries and administrative shapefiles using OSMnx and GeoPandas.

2️⃣ Data Preprocessing

Applied spatial subsetting to focus on Ranchi’s district boundaries.

Performed cloud filtering on Sentinel-2 datasets to improve NDVI accuracy.

Resampled data to monthly means for long-term analysis.

Converted MODIS (Kelvin → Celsius) and normalized NDVI values.

3️⃣ Risk Classification

Developed rule-based thresholds (e.g., LST > 35°C, NDVI < 0.3, humidity < 40%).

Labeled risk categories: Low, Medium, High, Extreme.

Trained a Random Forest Classifier on synthetic + real climate data to generalize risk detection.

4️⃣ Forecasting Models

ARIMA (Auto-Regressive Integrated Moving Average): Modeled historical temperature trends to forecast near-term urban heat risk.

LSTM (Long Short-Term Memory): Built a deep learning model to capture long-term seasonal dependencies in climate data.

Compared model performances and validated with error metrics (RMSE, MAE).

5️⃣ Impact Assessment & Insights

Assessed vegetation stress and crop productivity risks using NDVI-based thresholds.

Identified high-risk months and seasons for Ranchi’s population.

📷 Visualizations

Heatmaps of LST & NDVI

Climate trend plots (temperature, humidity, rainfall)

Risk classification maps

ARIMA vs LSTM forecast plots
