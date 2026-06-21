# Weather Forecasting MLOps Pipeline using Amazon SageMaker

## Project Overview

This project implements an end-to-end MLOps pipeline for weather forecasting using Amazon SageMaker. The pipeline covers data ingestion, feature management, model training, model evaluation, model registry, batch inference, and monitoring.

The objective is to demonstrate the complete machine learning lifecycle following MLOps best practices.

---

## Problem Statement

Accurate weather forecasting plays a critical role in environmental monitoring, disaster preparedness, agriculture, transportation, and urban planning.

This project uses historical weather data to predict temperature values based on atmospheric conditions such as humidity, wind speed, visibility, and pressure.

---

## Dataset

Source: Historical Weather Dataset

Features Used:

* Humidity
* Wind Speed (km/h)
* Wind Bearing (degrees)
* Visibility (km)
* Pressure (millibars)

Target Variable:

* Temperature (C)

Dataset Processing:

* Data cleaning
* Missing value handling
* Feature selection
* Train-Test split

---

## Project Architecture

```text
Weather Dataset
       │
       ▼
Data Ingestion
       │
       ▼
Amazon S3
       │
       ▼
Feature Store
       │
       ▼
Model Training
       │
       ▼
Model Registry
       │
       ▼
Batch Inference
       │
       ▼
Monitoring
```

---

## Technology Stack

* Python
* Pandas
* NumPy
* Scikit-Learn
* Amazon SageMaker
* Amazon S3
* Boto3
* GitHub

---

## Project Structure

```text
weather-forecasting-mlops/

├── data/
│   ├── weatherHistory.csv
│   ├── train.csv
│   └── test.csv
│
├── notebooks/
│   ├── 01_data_ingestion.ipynb
│   ├── 02_feature_store.ipynb
│   ├── 03_model_training.ipynb
│   ├── 04_model_registry.ipynb
│   ├── 05_batch_inference.ipynb
│   ├── 06_monitoring.ipynb
│   └── 07_pipeline_documentation.ipynb
│
├── models/
│   └── weather_model.pkl
│
├── outputs/
│   ├── predictions.csv
│   └── evaluation_metrics.csv
│
├── screenshots/
│
├── docs/
│
├── requirements.txt
└── README.md
```

---

## Model Training

Algorithm Used:

* Random Forest Regressor

Training Workflow:

1. Data Preprocessing
2. Feature Selection
3. Train-Test Split
4. Model Training
5. Performance Evaluation

---

## Model Evaluation Results

| Metric   | Value |
| -------- | ----- |
| MAE      | 4.20  |
| MSE      | 29.78 |
| R² Score | 0.677 |

---

## SageMaker Components Implemented

### Data Ingestion

* Historical weather dataset loaded and processed.

### Feature Store

* Weather features stored and managed using SageMaker Feature Store.

### Model Training

* Random Forest Regression model trained using processed weather data.

### Model Registry

* Model Package Group created for model version management.

### Batch Inference

* Predictions generated on unseen weather data.

### Monitoring

* Prediction error monitoring and drift analysis implemented.

---

## Results

The trained model successfully predicts temperature values based on weather conditions and demonstrates a complete MLOps workflow using Amazon SageMaker.

---

## Future Enhancements

* Real-time inference endpoint deployment
* Automated SageMaker Pipelines
* CI/CD integration using GitHub Actions
* Advanced forecasting using XGBoost and Deep Learning models
* Automated model retraining

---

## Authors
Team 7

Weather Forecasting MLOps Pipeline
