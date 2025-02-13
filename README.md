# Kaggle Competition: Sticker Sales Forecasting

## Overview
This project is part of a Kaggle competition aimed at forecasting sticker sales in different countries. The challenge evaluates predictions using the **Mean Absolute Percentage Error (MAPE)** metric.

## Dataset
The dataset consists of the following columns:
- **id**: Unique identifier for each record
- **date**: Date of sale
- **country**: Country of sale
- **store**: Store type
- **product**: Sticker product type
- **num_sold**: Number of stickers sold (Target variable)

## Objective
To build a robust model that accurately predicts the `num_sold` values while minimizing the MAPE score.

## Approach
### 1. Data Preprocessing
- Converted date column to datetime format
- Extracted additional features: month, day, day of week, and year
- Handled missing values (if any)
- Performed exploratory data analysis (EDA) to understand trends

### 2. Feature Engineering
- Created lag-based features for time series modeling
- Encoded categorical variables such as country, store, and product
- Applied seasonal decomposition to analyze trends and seasonality

### 3. Model Selection
- Tried multiple models including:
  - Linear Regression
  - Random Forest
  - Gradient Boosting (XGBoost, LightGBM, CatBoost)
  - Facebook Prophet
  - LSTM (Deep Learning)

### 4. Hyperparameter Tuning
- Used GridSearchCV and Bayesian Optimization for optimal parameter selection
- Implemented cross-validation to improve generalization

### 5. Final Model
- Selected **LightGBM** due to its performance and interpretability
- Fine-tuned hyperparameters and reduced overfitting with regularization

### 6. Evaluation
- Used Mean Absolute Percentage Error (MAPE) as the evaluation metric
- Achieved a competitive score on the leaderboard

## Results
| Model | MAPE Score |
|--------|------------|
| Linear Regression | 12.5% |
| Random Forest | 9.3% |
| XGBoost | 7.8% |
| LightGBM (Final) | 6.5% |

## Submission
- The final submission file contains two columns: `id` and `num_sold`
- Predictions were generated using the trained LightGBM model

## Future Improvements
- Implement advanced deep learning architectures
- Experiment with additional external data (e.g., holiday effects, economic indicators)
- Optimize hyperparameters further using automated tuning frameworks

## Conclusion
This competition provided insights into time series forecasting, feature engineering, and hyperparameter tuning. The final LightGBM model performed well in predicting sticker sales with a low MAPE score. Further improvements can be made by leveraging deep learning techniques and external data sources.

---

### Contact
For any questions, feel free to reach out to me:
- **Kaggle**: [@AshutoshJha-007](https://www.kaggle.com/AshutoshJha-007)
- **GitHub**: [AshutoshJha-007](https://github.com/AshutoshJha-007)
- **Email**: ashutosh.k.jha007@gmail.com
