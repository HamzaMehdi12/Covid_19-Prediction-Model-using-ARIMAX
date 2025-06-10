# Covid_19-Prediction-Model-using-ARIMAX

This codebase implements an ARIMAX modeling pipeline for COVID-19 case forecasting across four modular components. The dataset processing (dataset.py) handles temporal COVID-19 statistics through datetime conversion, feature engineering (lag features, day/month indicators), and preprocessing pipelines featuring Robust Scaling and mean imputation. It maintains temporal integrity during train/test splits (80/20) while generating visualization plots of case trends.

The model component (model.py) automates ARIMA parameter selection using pmdarima's auto_arima and fits an ARIMAX model with exogenous variables. Trained models are persisted via joblib serialization. The training orchestration (train.py) executes the core workflow: data loading → preprocessing → model training → forecast generation with confidence intervals. The evaluation module (evaluate.py) calculates regression metrics (MSE, MAE), compares forecasted versus actual values visually, and plots confidence bands around predictions.

## Key Features
The system focuses on forecasting daily new COVID-19 cases using time-series techniques while maintaining temporal relationships through strict datetime indexing. It features automated model configuration via auto_arima, integrated visual diagnostics at multiple stages, and robust preprocessing pipelines. The implementation handles exogenous variables through ARIMAX and provides confidence interval estimates for forecasts. The modular design separates concerns while maintaining interoperability between data processing, modeling, and evaluation components.

## Images
### Flow of Process
![Project Flow](https://github.com/user-attachments/assets/6471f781-8578-44a3-a853-f4aca6b3d66c)

### Daily Old and New Dataset for COVID_19
![Daily_Old_New_Deaths_Recovered_And_Total_Cases](https://github.com/user-attachments/assets/70d44b1b-9612-4b8f-b160-1cbd9a88979b)

### ARIMAX Train vs Test
![AriMAX Train vs Test Forecast](https://github.com/user-attachments/assets/aca6272d-a11e-4e54-b591-42f8240c460c)

### Results
![Results](https://github.com/user-attachments/assets/4a9015a2-e3b7-4ee0-b2ab-ccf185181fbf)
