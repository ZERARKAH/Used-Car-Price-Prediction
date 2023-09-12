

# Used Car Price Prediction: A CRISP-DM Approach

## Overview

This repository employs the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology to analyze a dataset of used car listings. The dataset, sourced from Kaggle, originally consisted of 3 million entries; however, for computational efficiency, we focus on a subset of 426K entries. The primary goal is to identify factors that influence the pricing of used cars, thereby aiding a used car dealership in making informed decisions.

## CRISP-DM Process

### 1. Business Understanding

The core objective is to provide actionable recommendations to a used car dealership about what attributes or features consumers most value in a used car. Understanding these can enable the dealership to price their cars more effectively and improve profitability.

### 2. Data Understanding

- **Source**: Kaggle
- **Size**: 426K entries after preprocessing
- **Features**: Year, Manufacturer, Model, Condition, Odometer Reading, Title Status, Paint Color
- **Target Variable**: Price (in USD)

### 3. Data Preparation

Data preprocessing involved multiple steps:
- Handling missing values
- Removing outliers
- Feature engineering, including one-hot encoding and normalization

### 4. Modeling

Three types of regression models were employed:
- Linear Regression
- Ridge Regression
- LASSO Regression

Hyperparameters were tuned using GridSearchCV.

### 5. Evaluation

Models were evaluated based on:
- \( R^2 \) Score: Proportion of the variance in the dependent variable that is explained by the independent variables
- RMSE: Root Mean Squared Error

### 6. Deployment

The final models can be used by the used car dealership to predict car prices based on the features. Continuous monitoring and updating are recommended for maintaining accuracy.

## Key Findings

### Data Characteristics

1. **Popular Makes and Models**: The dataset predominantly features common makes and models, offering a realistic snapshot of the used car market.
  
2. **Price and Mileage Variability**: Prices and odometer readings showed wide ranges, including some outliers at both extremes.

### Model Performance

1. **Comparable Performance**: Linear Regression, Ridge Regression, and LASSO Regression exhibited similar performance metrics on the dataset.

2. **Strong Predictive Power**: All three models achieved an \( R^2 \) score above 0.8 on the test set, meaning they could explain more than 80% of the variance in car prices.

3. **Residual Distribution**: The residuals for all three models were generally well-distributed around zero, although there was some indication of heteroscedasticity (varying spread of residuals across the range of predicted values).

### Variable Importance

1. **Year and Condition**: Cars that are newer and in better condition generally command higher prices, as intuitively expected.

2. **Manufacturer and Model**: Certain car brands and models tend to be more expensive, likely owing to brand value, luxury status, or other factors that influence perceived quality.

3. **Mileage**: Lower odometer readings generally lead to higher prices, which is consistent with the expectation that cars with less wear and tear are more valuable.

## Recommendations for the Used Car Dealership

1. **Stock Popular Models**: Given that the top 50 most common models in the dataset are also likely to be the most traded, these should be the dealership's focus.

2. **Quality Over Quantity**: The data suggests that cars in better condition and with lower mileage can command higher prices. The dealership might consider focusing on these types of cars.

3. **Newer is Better**: Generally, newer cars are priced higher. Therefore, keeping a stock of newer used cars could be beneficial for the dealership.

4. **Continuous Data Monitoring**: As the used car market is dynamic, it would be advisable to regularly update the pricing model with new data for more accurate and competitive pricing.


- Newer cars and cars in better condition are generally priced higher.
- Certain manufacturers and models command higher prices, possibly due to brand value or luxury status.
- Lower odometer readings are correlated with higher prices.

## Recommendations

- Focus on acquiring popular models and brands that are known to hold value.
- Prioritize cars that are in better condition and have lower odometer readings.
- Regularly update the pricing model with fresh data to adapt to market changes.

## Usage

The Jupyter notebook in this repository contains all the code for data preprocessing, modeling, and evaluation.

## Contributing

Contributions are welcome. Feel free to fork the repository and submit pull requests.

## License

Hamza ZERARKA

#
