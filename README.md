# Amazon Delivery Time Prediction

## Overview
Predict delivery times for e-commerce orders using geospatial, temporal, and contextual features. Trains multiple regressors and exposes a Streamlit app for inference. MLflow is used to track experiments.

## Files
- `amazon_delivery.csv` : raw dataset (not included here)
- `data_preparation.py` : raw -> cleaned data
- `feature_engineering.py` : create derived features
- `final_features.csv` : features used for modeling (output)
- `eda.py` : exploratory plots saved to `plots/`
- `model_training.py` : trains models and logs to MLflow
- `predict.py` : helper to load model and predict
- `app.py` : Streamlit app to interact with model
- `requirements.txt` : environment requirements

## How to run
1. Create a virtual environment and install requirements:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```
2. Prepare data:
   ```bash
   python data_preparation.py
   python feature_engineering.py
   ```
3. Run EDA (optional):
   ```bash
   python eda.py
   ```
4. Train models & log with MLflow:
   ```bash
   python model_training.py
   ```
   To view MLflow UI:
   ```bash
   mlflow ui --port 5000
   ```
5. Run Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Notes
- Place `amazon_delivery.csv` in the project root before running.
- MLflow creates `mlruns/` to store experiments and models.
```

---

## File: architecture.png

*(Add a simple architecture diagram showing flow: Data -> Cleaning -> Feature Eng -> Model Training (MLflow) -> Streamlit App. This file placeholder reminds you to include an image.)*

---

## File: model_performance_summary.csv (template)
```
model,MAE,RMSE,R2
LinearRegression,,,
RandomForest,,,
GradientBoosting,,,
```
