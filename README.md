Hotel Booking ADR Prediction
Project Overview
This project aims to predict the Average Daily Rate (ADR) for hotel bookings using machine learning. We leverage historical booking data to identify key factors influencing pricing strategies and implement predictive models to forecast ADR, optimizing revenue management.

Features and Models
We've developed models based on features like room type, customer demographics, and booking details. Our models include:

Linear Regression
Ridge Regression
Lasso Regression
Decision Tree
Gradient Boosting
XGBoost
The models are evaluated based on Mean Squared Error (MSE) and R-squared metrics.

Model Comparisons
Figure 1: Performance comparison of various models.

Hyperparameter Tuning
Extensive grid search and cross-validation techniques were employed to fine-tune the models, particularly XGBoost, which demonstrated superior performance.

Hyperparameter Tuning
Figure 2: Hyperparameter tuning results.

Correlation Analysis
A correlation matrix was constructed to discern the relationships between different features and ADR, guiding the feature selection process.

Correlation Matrix
Figure 3: Heatmap showing feature correlations with ADR.

Seasonal Trends
Seasonal trends in ADR were analyzed to understand the impact of time-related factors on hotel pricing.

Seasonal Trends
Figure 4: Seasonal ADR trends by month and year.

Getting Started
To run this project locally:

Clone the Repo: https://github.com/suhas-km/Hotel-Booking-Data-Science.git


Contributing
Contributions are welcome! Please read the contributing guide for details on our code of conduct, and the process for submitting pull requests.

License
This project is licensed under the MIT License - see the LICENSE file for details.
