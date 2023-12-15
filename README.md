# Hotel Booking ADR Prediction 🏨💰

## Project Overview 📈
**This project aims to predict the Average Daily Rate (ADR) for hotel bookings using machine learning**. We leverage historical booking data from a [2019 paper](https://pdf.sciencedirectassets.com/311593/1-s2.0-S2352340918X00079/1-s2.0-S2352340918315191/main.pdf?X-Amz-Security-Token=[[...long url here...](https://pdf.sciencedirectassets.com/311593/1-s2.0-S2352340918X00079/1-s2.0-S2352340918315191/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEPX%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIAy6RTtnqnIriNQ8Kp3%2FgHk7snFUG00VPOJew3AE8VMWAiEAqGpMe6TgMri2G9Qc%2B2hCxH6bR4i1qcmebYGmn4XYo6AqswUIbRAFGgwwNTkwMDM1NDY4NjUiDE8BoiJvSSUDmjgonyqQBfgTfZ5vL%2F8ZawXqJHtUi604ARM9D0Oxj0AMVGN0NIigTQXJLvIOdpXSn1TC7Jwba5s4dQvGxXp8inZuvdGw6kRjFjk6Tkk8i4TvG04hkXayLMf6dobj59J9JOgAQcdbyPcQy%2Bf7xPcS4SZIINGYuUsgPGH95i1tgaOKciZUMb7yayucrsLwjRCQCqDlC7ji78UCwxu%2FdrJCOWGgzoY1tevwhMJ1rmqOH6FTp%2BQolKmvgpsGRZl2wOeokDINURohyWIbW%2Fc4GN3CckEK4LhvHYdgmEgdh%2F3XiNZjGnTLOMKw3u1IQ48BMZI4F0fV6DQ39OiQkC5iAWc30LuSOgfo0J0TpZmm8ffvRGR5%2B5SPoLjzRf1ZWivQIIUCI9gzzbSiRjYe7fPvEmzdiFzEy5dCIgrMIxJ0ktAXqFLlvwkvnSyOoIq0hjsWFknaq5UK0VfrRV2LKqcG9U3eyKtAkCTXl5qGNLEqyccoUmF3O2rIKLeKKjXbg0QYIcdDzez%2FbbUJ%2FXri2Fp4JBjr%2B5JFv5arttaS%2Bvbmh2oNdTB2E5Qzge%2FG9OhUxaLXWIaNGXby1EH3CRSO12zQcmRvdhSzqW%2FQ5o6wHp7oD%2F4ll3GoUvDRwuWE%2FhK2cTwcIJChfXNmibfowVM4XIBAnuTzXbodALsEzcUTxAGbpSkCKF0iKqBp%2BR7nVbQO6NzNZunDiqdW8gHk4MqVB1nc1ZfOP7sLBhhP5iF6AT2%2BielbAm4nr%2F7mPVGFXcoDOeSqDAr1%2BObFF2v%2BAf0NYvb9N5TXpXAue%2BpewyrM7L2Sl0hXbdUxtzJGzCC1zN1Fp%2BlAZzudOuXvLc%2BxInxF%2BSFfasGU3wzPkNFoKtAGV7QaEkrkG13mqdwyWotoMOmi76sGOrEB8Kl%2BBdp2xcIxeuVMW0PAX%2FIEESHUva9LYWXF2DyNeiPH1p4dF48KnlRjinBbcoUYLqy041WN0FWSqYjsM9d8169WMUs6jNfZwe8VB49svaY%2FSH71MbD%2B5qo73fov%2BRb3Bj%2F35gL67mV019AMZjJs9v3NbLqOW4xK7wefy3xB12LWU%2Fdn4M%2BLYAOkQ1%2B19Hr5DI0RhMFZXszoT8SkdTiWm1dOtEFU0b%2Fr91Wjhi%2BFo1Zx&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20231215T045242Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYTXEAIHMA%2F20231215%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=cbffdd4952123694d78383adc19133caec4a0f5aff1abe681eec65c4813ed39d&hash=43a56e88eb81e54d794a985c2e20d1019928db54c9b8998dae2524148eddb1fa&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S2352340918315191&tid=spdf-9d198631-39af-471e-b552-62fa64e8a6e4&sid=e2831aaf673af74c503a545542fd640d069egxrqa&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=0f135a51530455555255&rr=835c14245cae829c&cc=us)https://pdf.sciencedirectassets.com/311593/1-s2.0-S2352340918X00079/1-s2.0-S2352340918315191/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEPX%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIAy6RTtnqnIriNQ8Kp3%2FgHk7snFUG00VPOJew3AE8VMWAiEAqGpMe6TgMri2G9Qc%2B2hCxH6bR4i1qcmebYGmn4XYo6AqswUIbRAFGgwwNTkwMDM1NDY4NjUiDE8BoiJvSSUDmjgonyqQBfgTfZ5vL%2F8ZawXqJHtUi604ARM9D0Oxj0AMVGN0NIigTQXJLvIOdpXSn1TC7Jwba5s4dQvGxXp8inZuvdGw6kRjFjk6Tkk8i4TvG04hkXayLMf6dobj59J9JOgAQcdbyPcQy%2Bf7xPcS4SZIINGYuUsgPGH95i1tgaOKciZUMb7yayucrsLwjRCQCqDlC7ji78UCwxu%2FdrJCOWGgzoY1tevwhMJ1rmqOH6FTp%2BQolKmvgpsGRZl2wOeokDINURohyWIbW%2Fc4GN3CckEK4LhvHYdgmEgdh%2F3XiNZjGnTLOMKw3u1IQ48BMZI4F0fV6DQ39OiQkC5iAWc30LuSOgfo0J0TpZmm8ffvRGR5%2B5SPoLjzRf1ZWivQIIUCI9gzzbSiRjYe7fPvEmzdiFzEy5dCIgrMIxJ0ktAXqFLlvwkvnSyOoIq0hjsWFknaq5UK0VfrRV2LKqcG9U3eyKtAkCTXl5qGNLEqyccoUmF3O2rIKLeKKjXbg0QYIcdDzez%2FbbUJ%2FXri2Fp4JBjr%2B5JFv5arttaS%2Bvbmh2oNdTB2E5Qzge%2FG9OhUxaLXWIaNGXby1EH3CRSO12zQcmRvdhSzqW%2FQ5o6wHp7oD%2F4ll3GoUvDRwuWE%2FhK2cTwcIJChfXNmibfowVM4XIBAnuTzXbodALsEzcUTxAGbpSkCKF0iKqBp%2BR7nVbQO6NzNZunDiqdW8gHk4MqVB1nc1ZfOP7sLBhhP5iF6AT2%2BielbAm4nr%2F7mPVGFXcoDOeSqDAr1%2BObFF2v%2BAf0NYvb9N5TXpXAue%2BpewyrM7L2Sl0hXbdUxtzJGzCC1zN1Fp%2BlAZzudOuXvLc%2BxInxF%2BSFfasGU3wzPkNFoKtAGV7QaEkrkG13mqdwyWotoMOmi76sGOrEB8Kl%2BBdp2xcIxeuVMW0PAX%2FIEESHUva9LYWXF2DyNeiPH1p4dF48KnlRjinBbcoUYLqy041WN0FWSqYjsM9d8169WMUs6jNfZwe8VB49svaY%2FSH71MbD%2B5qo73fov%2BRb3Bj%2F35gL67mV019AMZjJs9v3NbLqOW4xK7wefy3xB12LWU%2Fdn4M%2BLYAOkQ1%2B19Hr5DI0RhMFZXszoT8SkdTiWm1dOtEFU0b%2Fr91Wjhi%2BFo1Zx&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20231215T045242Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYTXEAIHMA%2F20231215%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=cbffdd4952123694d78383adc19133caec4a0f5aff1abe681eec65c4813ed39d&hash=43a56e88eb81e54d794a985c2e20d1019928db54c9b8998dae2524148eddb1fa&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S2352340918315191&tid=spdf-9d198631-39af-471e-b552-62fa64e8a6e4&sid=e2831aaf673af74c503a545542fd640d069egxrqa&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=0f135a51530455555255&rr=835c14245cae829c&cc=us]) to identify key factors influencing pricing strategies and implement predictive models to forecast ADR, optimizing revenue management.

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
Contributions are welcome! Please read the [contributing guide](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

## License 📜
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE.md) file for details.
