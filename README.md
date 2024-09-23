
# House Price Prediction: Ames Housing Market

This repository contains an analysis of house prices in the Ames housing market, using data from the Ames Housing Dataset. The objective of this project is to build a predictive model to estimate house prices based on various housing characteristics.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Research Question](#research-question)
- [Methodology](#methodology)
- [Results](#results)
- [Usage](#usage)
- [Conclusions](#conclusions)
- [Limitations](#limitations)
- [Future Work](#future-work)
- [License](#license)

## Project Overview

This project explores the relationship between several housing characteristics and their impact on house prices. We aim to develop a regression model that can predict house prices in Ames, Iowa, based on features such as lot area, overall quality, indoor square footage, and kitchen quality.

## Dataset

The dataset used in this project is the **Ames Housing Dataset**, which provides detailed information on over 1,400 houses. Key variables include:

- **SalePrice**: The price at which the house was sold (dependent variable)
- **LotArea**: Size of the lot (in square feet)
- **OverallQual**: Overall material and finish quality of the house (ordinal scale)
- **OverallCond**: Overall condition of the house (ordinal scale)
- **InSF**: Total indoor square footage (calculated)
- **OutSF**: Total outdoor square footage (calculated)
- **KitchenQual**: Kitchen quality (ordinal scale)

[Link to the dataset](https://www.kaggle.com/datasets/prevek18/ames-housing-dataset)

## Research Question

**Objective**: To develop a model that accurately predicts house prices based on several independent variables, including lot area, overall quality, overall condition, indoor square footage, outdoor square footage, and kitchen quality.

**Hypothesis**: Fundamental housing characteristics, such as square footage and overall quality, are significant predictors of house price.

## Methodology

1. **Data Preprocessing**:
   - Selected relevant features and handled missing data.
   - Created new variables: `InSF` (indoor square footage) and `OutSF` (outdoor square footage).
   - Converted `KitchenQual` into a numeric scale for regression analysis.

2. **Exploratory Data Analysis**:
   - Visualized the distribution of house prices and other variables.
   - Examined relationships between predictor variables and house prices using scatter plots and correlation analysis.

3. **Modeling**:
   - Built a multiple linear regression model with the following predictors: `LotArea`, `OverallQual`, `OverallCond`, `InSF`, `OutSF`, and `KQual`.
   - Evaluated the model using metrics such as R-squared and F-statistics.

## Results

The model showed that several housing characteristics have a significant relationship with sale price, with the following key findings:

- **OverallQual** and **InSF** were the strongest predictors of house price, with correlation coefficients of 0.791 and 0.808, respectively.
- **LotArea** and **OutSF** had weaker but still significant correlations with house price.
- The regression model achieved an **R-squared value of 77.7%**, indicating that the model explains 77.7% of the variance in house prices.

### Key Plots and Correlations:

- **OverallQual vs. SalePrice**: Higher quality homes tend to have higher sale prices.
- **InSF vs. SalePrice**: Larger indoor spaces are associated with higher prices.
- **LotArea vs. SalePrice**: Larger lots contribute to higher sale prices, though the relationship is less pronounced.

## Usage

To run this analysis on your local machine:

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/house-price-prediction-ames.git
   ```
2. Navigate to the project directory:
   ```bash
   cd house-price-prediction-ames
   ```
3. Install the required dependencies (using R or Python, depending on your setup):
   ```bash
   # For R
   install.packages(c('tidyverse', 'psych', 'ggpubr', 'car'))

   # For Python (if converting to Python)
   pip install -r requirements.txt
   ```
4. Run the analysis script or Jupyter notebook to replicate the results.

## Conclusions

- **Significant Predictors**: Overall quality and indoor square footage are the most influential factors in predicting house prices in Ames, Iowa.
- **Model Performance**: The linear regression model explains 77.7% of the variance in house prices, making it a useful tool for house price prediction in this market.
- **Business Implications**: Real estate companies and individual buyers can use the model to estimate fair prices for houses based on core characteristics, helping them make informed decisions.

## Limitations

1. **Ames-Specific Data**: The dataset only covers houses in Ames, Iowa, so generalizing the results to other housing markets may be inappropriate.
2. **Subjectivity in Variables**: Variables like **OverallQual** and **KitchenQual** are subjective and may not be consistently applied across datasets or assessors.
3. **Unexplained Variation**: The model leaves about 22% of the variance in house prices unexplained, which may be due to external factors not included in the dataset.

## Future Work

- Expand the dataset to include houses from other markets to test the generalizability of the model.
- Include economic and financial variables (e.g., average time on the market, mortgage rates) to further improve the model’s predictive power.
- Investigate more advanced machine learning techniques (e.g., random forest, gradient boosting) to potentially increase prediction accuracy.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
