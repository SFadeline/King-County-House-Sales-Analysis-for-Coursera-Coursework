# King County House Sales Analysis

A Python project exploring house prices in King County, Washington, USA, and comparing regression models for price prediction.

This project was completed as part of IBM’s **Data Analysis with Python** course on Coursera.

## Project Objective

Explore how property characteristics—including living area, grade, location, and waterfront status—relate to house prices, then build and evaluate prediction models.

## Tools and Libraries

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Dataset

The dataset contains 21,613 house sale records and includes features such as:

- Price
- Bedrooms and bathrooms
- Living area and lot size
- Number of floors
- Waterfront status
- Property grade and condition
- Latitude and longitude

The dataset was provided through IBM Skills Network for the course assignment.

## Analysis Workflow

1. Inspect column data types and summary statistics.
2. Remove unnecessary identifier columns.
3. Replace missing bedroom and bathroom values with their column means.
4. Count houses by floor values.
5. Explore prices using box plots, regression plots, and correlations.
6. Fit simple and multiple linear regression models.
7. Build a pipeline with scaling and polynomial features.
8. Evaluate Ridge regression using a training/test split.

## Key Findings

- Above-ground living area has a positive correlation with price.
- Living area and property grade have stronger correlations with price than several other numeric features.
- Using multiple features improves the training fit compared with using living area alone.
- Polynomial Ridge regression achieves a higher test R² than Ridge regression using the original features.

## Model Results

| Model | Evaluation Data | R² |
|---|---|---:|
| Linear regression: living area only | Training | 0.4929 |
| Multiple linear regression | Training | 0.6577 |
| Scaling + polynomial features + linear regression | Training | 0.7512 |
| Ridge regression, alpha = 0.1 | Test | 0.6479 |
| Second-order polynomial + Ridge, alpha = 0.1 | Test | 0.7003 |

Training scores describe fit to the data used to train the model. Test scores measure performance on held-out data, so these two types of scores should not be directly ranked together.

## Project File

[View the completed notebook](House_Sales_in_King_Count_USA.ipynb)

The notebook includes the code, saved outputs, and visualizations.

## Limitations and Future Improvements

- Missing values were filled before splitting the data, following the course workflow. A future version should fit imputation using training data only.
- The results use one training/test split.
- Future work could include cross-validation, hyperparameter tuning, and analysis of prediction errors.

## Acknowledgements

The assignment template and dataset were provided by IBM Skills Network as part of the Data Analysis with Python course. This repository contains my completed coursework.
