# celebal-tech-early-fault-prediction

The project entailed early fault prediction in sensors, utilizing machine learning models such as Random Forest, Support Vector Machine, and Gradient Boosting for predictive analysis. Key concepts included feature engineering, model optimization, and cross-validation to ensure accuracy and robustness in early fault detection.

Major Reference:
- Griffin, S. (2022). _machine_failure_. Retrieved from https://github.com/shadgriffin/machine_failure [15th July 2023]


# Machine Failure Prediction with Decision Tree-Based Regressors
## Overview
This project aims to predict the remaining time until a machine failure using various decision tree-based regression models. By analyzing historical sensor data, the models can provide early warnings for potential machine failures, enabling preventive maintenance and reducing downtime.
Decision Tree-Based Regressors
What are Decision Tree-Based Regressors?

Decision tree-based regressors use a tree-like structure to make predictions. They split the data into branches based on feature values and make predictions at the leaf nodes. These models can capture non-linear relationships and are easy to interpret, though they are prone to overfitting if not properly controlled.
## Models Used
### XGBRegressor

The XGBRegressor is a gradient boosting algorithm that builds an ensemble of decision trees, where each tree corrects the errors of the previous ones. This sequential training process enhances the model's accuracy. Key features include:

    Regularization: To prevent overfitting.
    Parallelization: Optimized for performance.
    Hyperparameters: Includes n_estimators, max_depth, learning_rate, and more.

### Random Forest Regressor

The RandomForestRegressor is an ensemble method that constructs multiple decision trees in parallel and averages their predictions. It introduces randomness in feature selection and data sampling, which helps reduce overfitting and improves generalization. Key features include:

    Bagging: Random sampling of data for each tree.
    Feature Randomness: Random selection of features for splits.
    Resilience to Noise: Handles noisy data better than individual trees.

### LightGBM

LightGBM is another gradient boosting framework similar to XGBoost but optimized for speed and memory efficiency. It uses a histogram-based approach and grows trees leaf-wise rather than level-wise, making it faster and more efficient on large datasets. Key features include:

    Efficiency: Faster training and lower memory consumption.
    Categorical Features: Supports categorical variables directly.
    Leaf-wise Growth: Focuses on the most significant splits first.

## Lag Features (Rolling Mean and Standard Deviation)

The code introduces lagged features, specifically rolling means and rolling standard deviations, to capture temporal dependencies in the sensor data. These features help the model understand how past sensor readings influence future outcomes, enhancing its predictive power.

For example:

    Rolling Mean: Captures trends over time.
    Rolling Standard Deviation: Measures the volatility or stability in the sensor readings.

These features are used in conjunction with the original sensor data to improve the prediction of the remaining time to failure.
