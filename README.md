# Energy Efficiency Modeling (Regression)

This project uses machine learning regression models to predict **heating** and **cooling loads** in residential buildings based on architectural and design characteristics. The goal is to support energy-efficient decision-making in the early design phase.

## Project Structure

```
├── Energy_efficiency_modeling_regression.ipynb   # Main analysis notebook
├── README.md                                     # Project documentation
├── data/
│   └── energy_efficiency_data.csv                # Dataset used for modeling
```


## Dataset

The dataset comes from the [UCI Energy Efficiency Data Set](https://archive.ics.uci.edu/ml/datasets/Energy+efficiency), consisting of 768 samples with the following input features:

- Relative Compactness
- Surface Area
- Wall Area
- Roof Area
- Overall Height
- Orientation
- Glazing Area
- Glazing Area Distribution

**Target Variables:**

- Heating Load (Y1)
- Cooling Load (Y2)

## Models Applied

- Linear Regression (baseline model)

- Catboosting Regressor

- Random Forest Regressor

- Gradient Boosting Regressor

## Evaluation Metrics (Catboosting Regressor-- Best Performing Model)

| Target Variable |   MAE    | R² Score |
|-----------------|----------|----------|
| Heating Load    | ~0.2374  | ~0.9987  |
| Cooling Load    | ~0.4765  | ~0.9949  |



The Catboosting Regressor significantly outperformed other models, achieving near-perfect R² scores (~0.99) for both target variables.

## Key Insights

- Roof area, overall height, and surface area were key predictors for heating load.
- Overall height, roof area, and relative compactness were key predictors for cooling load.
- Catboosting Regressor outperformed simpler models by capturing complex, nonlinear relationships.


