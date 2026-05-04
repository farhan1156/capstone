# Capstone Notebook

This repository contains a Python notebook for exploratory data analysis, outlier detection, visualization, and basic modeling on a delivery dataset.

## Contents

- `driver.ipynb` - main notebook that loads data, cleans it, analyzes outliers, creates visualizations, and trains simple prediction models.
- `[data/data.csv](https://www.kaggle.com/datasets/waddahali/order-delivery-dataset?resource=download)` - source dataset used by the notebook.

## Requirements


- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn

## How to run

1. Open `driver.ipynb` in Jupyter Notebook or JupyterLab.
2. Run the notebook cells sequentially.
3. Ensure `data/data.csv` is available and readable.

## Notebook workflow

1. Import required libraries.
2. Read the dataset from `data/data.csv`.
3. Clean the data:
   - remove duplicate rows
   - check for missing values
   - drop missing rows if any
4. Detect and label outliers using `IsolationForest`.
5. Remove outlier rows and store the cleaned dataset in `df_no_outliers`.
6. Generate visualizations, including:
   - `Total_Price` distribution
   - delivery duration by city
   - payment method distribution
   - driver vehicle vs delivery distance
   - order status distribution
   - distance vs duration scatter plot
7. Perform feature extraction and encoding for model preparation.
8. Train a baseline logistic regression model for `Order_Status`.
9. Train a random forest regressor to predict `Delivery_Duration_Minutes`.

## Notes

- The notebook saves an outlier analysis pairplot image to `img/outlier_analysis_pairplot.png` if the `img` folder exists.
- Feature engineering includes converting timestamp columns to hour and weekday features and encoding categorical variables.
- The project demonstrates both classification and regression modeling on the cleaned delivery dataset.
