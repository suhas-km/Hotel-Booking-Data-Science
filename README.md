# Hotel Booking ADR Prediction 🏨💰

Project Overview 📈
This project aims to predict the Average Daily Rate (ADR) for hotel bookings using machine learning. We leverage publicly available historical booking data from a 2019 paper related to Portugal Hospitality Data.


Kaggle: https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand

## Features and Models 🛠️
We've developed models based on features like room type, customer demographics, and booking details. Our models include:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Decision Tree**
- **Gradient Boosting**
- **XGBoost**

The models are evaluated based on **Mean Squared Error (MSE)** and **R-squared** metrics.

### Model Comparisons 📊
*Performance comparison of various models.*

## Hyperparameter Tuning 🔧
Extensive grid search and cross-validation techniques were employed to fine-tune the models, particularly **XGBoost**, which demonstrated superior performance.

### Hyperparameter Tuning 📈
*Hyperparameter tuning results.*

## Correlation Analysis 🔍
A correlation matrix was constructed to discern the relationships between different features and ADR, guiding the feature selection process.

### Correlation Matrix 📉
*Heatmap showing feature correlations with ADR.*

## Seasonal Trends 📅
Seasonal trends in ADR were analyzed to understand the impact of time-related factors on hotel pricing.

### Seasonal Trends 🌞❄️
*Seasonal ADR trends by month and year.*

## Getting Started 🚀
To run this project locally:
1. **Clone the Repo:** `git clone https://github.com/suhas-km/Hotel-Booking-Data-Science.git`

## Contributing 🤝
Contributions are welcome! Please do consider clonning and contributing. Do reach out to me for details, and the process for submitting pull requests.
