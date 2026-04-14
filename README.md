## Key Results

- Sentiment improves LSTM performance in short-term prediction (1-day horizon)
- Machine Learning models benefit more from sentiment in longer horizons (5-day)
- More complex sentiment features do not always improve results (FULL vs SIMPLE)

## Project Highlights

- End-to-end Data Science project (data → modeling → evaluation)
- Comparison between ML and Deep Learning approaches
- Use of NLP (FinBERT) for financial sentiment analysis
- Time-series validation avoiding data leakage
  

# S&P 500 Direction Prediction using Machine Learning and Deep Learning

This project is based on my Master's Thesis in Artificial Intelligence, where I analyze whether incorporating sentiment extracted from financial news improves the prediction of the S&P 500 index direction.

## Objective

To evaluate the incremental predictive value of sentiment variables derived from financial headlines in a binary classification problem (market up/down).

## Approach

The study is designed as a controlled experiment comparing three scenarios:

- **BASE**: Only financial variables derived from returns
- **SIMPLE**: Adds daily aggregated sentiment (mean + news volume)
- **FULL**: Includes additional sentiment features (median, std, sentiment ratios)

The comparison is performed under consistent conditions (same splits, preprocessing, and models) to isolate the effect of sentiment.

## Data

- S&P 500 historical data (Yahoo Finance)
- Financial news dataset (Kaggle)
- Sentiment extracted using FinBERT (Hugging Face)

## Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Hugging Face Transformers (FinBERT)
- Matplotlib

## Models

### Machine Learning
- Logistic Regression
- Random Forest
- Gradient Boosting
- Dummy baseline

### Deep Learning
- LSTM Neural Networks

## Methodology

- Time series prediction (1-day and 5-day horizons)
- Feature engineering (lags, moving averages, volatility)
- Sentiment aggregation at daily level
- Strict temporal validation to avoid data leakage
- Hyperparameter tuning using TimeSeriesSplit

## Evaluation Metrics

- ROC-AUC
- Balanced Accuracy
- F1-score
- Precision / Recall

## Results

Key findings:

- Sentiment improves performance in:
  - LSTM models for short-term prediction (1-day horizon)
  - Machine Learning models for medium-term prediction (5-day horizon)
- The effect of sentiment depends on both the prediction horizon and model type
- More complex sentiment features (FULL) do not always outperform simpler ones (SIMPLE)

## Repository Structure

/data -> datasets used in the project

/notebooks -> experimentation and model development

/results -> model outputs and evaluation

## Author

Jesús Daniel Romeral Cortina  
Master in Artificial Intelligence
