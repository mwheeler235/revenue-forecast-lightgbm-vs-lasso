# Coffee Sales Revenue Forecasting

Our goals are to understand the best granularity for modeling coffee revenue across coffee types and to evaluate multiple models for revenue forecasting. After performing EDA, I chose to predict weekly coffee revenue (with analysis by coffee type) using LightGBM and Lasso regression models.

## Features

- **Time series forecasting** of weekly coffee revenue by coffee type
- **Feature engineering** including lag features, rolling averages, and seasonal patterns
- **Model comparison** between LightGBM and Lasso regression
- **Cross-validation** for LightGBM model
- **Performance evaluation** across 8 different coffee types

## Key Results

| Model | Overall R² | MAPE | Features Used |
|-------|------------|------|---------------|
| **Lasso** | 0.735 | 31.2% | 11/25 selected |
| LightGBM | 0.517 | 39.3% | 25 features |

## Models Evaluated

1. **Combined LightGBM**: Single model trained on all coffee types
2. **Separate LightGBM**: Individual models per coffee type  
3. **Lasso Regression**: Linear model with automatic feature selection

## Dependencies

- pandas, numpy
- scikit-learn  
- lightgbm
- matplotlib

## Dataset

Kaggle data acquired from: (https://www.kaggle.com/datasets/minahilfatima12328/daily-coffee-transactions/data).