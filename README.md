# Car-Price-Prediction
Predicting Car Prices using Linear Regression 
# Car Price Prediction

## Overview
This project predicts car prices using machine learning techniques. By analyzing various car features like horsepower, torque, age, and top speed, the model can estimate the current market price of a vehicle.

## Table of Contents
- [Requirements](#requirements)
- [Dataset](#dataset)
- [Model Description](#model-description)
- [Results](#results)
- [Usage](#usage)
- [Future Improvements](#future-improvements)

## Requirements
The following libraries are required to run this project:
```
pandas
seaborn
matplotlib
scikit-learn
```

Install the dependencies using:
```bash
pip install pandas seaborn matplotlib scikit-learn
```

## Dataset
The project uses the `car_price_prediction.csv` dataset containing information about various car models and their prices. Key features include:
- On Road Old
- On Road now
- Rating
- Condition
- Economy
- kilometers (km)
- Horsepower (hp)
- Torque
- Age (years)
- Top speed
- Current price (target variable)

## Model Description
The project implements two linear regression models:
1. **Initial Model**: Uses all available features to predict car prices.
2. **Optimized Model**: Removes features with correlation values less than 0.03 with the target variable (current price). The removed features include torque, hp, years, and top speed.

The data is split into training (80%) and testing (20%) sets using a random state of 42 for reproducibility.

## Results
The model evaluation includes:
- Comparison between predicted and actual prices
- Visualization of feature relationships using pair plots
- Correlation analysis to identify the most influential features

Both models are evaluated using the R² score, which measures the proportion of variance in the dependent variable that can be predicted from the independent variables.

## Usage
1. Clone this repository:
```bash
git clone https://github.com/yourusername/car-price-prediction.git
cd car-price-prediction
```

2. Place your `car_price_prediction.csv` file in the project directory.

3. Run the Jupyter notebook or Python script:
```bash
jupyter notebook car_price_prediction.ipynb
```
or
```bash
python car_price_prediction.py
```

## Feature Engineering
The project explores feature selection based on correlation analysis:
1. Calculate correlation between features and target variable
2. Remove features with correlation values less than 0.03
3. Train a new model on the reduced feature set
4. Compare performance between the full-feature and reduced-feature models

## Future Improvements
- Implement more advanced regression techniques (Random Forest, Gradient Boosting)
- Add feature engineering to create more predictive variables
- Perform hyperparameter tuning to optimize model performance
- Explore non-linear relationships between features and price
- Address potential multicollinearity between features
- Incorporate categorical variables with one-hot encoding

## Contribution
Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss the proposed changes.

## License
[Apache 2.0 License](LICENSE)
