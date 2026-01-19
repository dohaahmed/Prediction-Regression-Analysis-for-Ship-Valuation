# Prediction-Regression-Analysis-for-Ship-Valuation
Regression-based modeling project for predicting ship sale prices using Age, DWT, and BDI market index variables. Includes EDA, feature scaling, model diagnostics, and scenario analysis.

## Project Overview
This project applies predictive analytics and regression modeling to estimate the market value of capesize ships based on vessel characteristics and market conditions. Using historical transaction data, I built and evaluated both simple linear regression and multiple linear regression models to generate accurate ship price predictions and support valuation decisions.

The analysis is based on a case study involving the valuation of the ship "Bet Performer", with the goal of producing a defensible estimated fair market price under different market scenarios.

## Objectives
• Explore ship sale transaction data and identify key price drivers
• Build a Simple Regression Model (Price ~ Age)
• Build a Multiple Regression Model (Price ~ Age + DWT + BDI)
• Evaluate model quality using R²/Adjusted R², t-tests, p-values, and regression diagnostics
• Generate point predictions, 95% Confidence Intervals, and 95% Prediction Intervals
• Perform scenario analysis to adjust valuation for different assumptions

## Dataset
The dataset contains ship sale transactions with the following key variables:

Price: Ship sale price (USD millions)
Age: Vessel age at sale (years)
DWT: Deadweight tonnage (thousands of tons)
BDI: Baltic Dry Index (market indicator)

Note: The dataset was cleaned and prepared for modeling, including formatting, numeric conversion, and feature engineering (e.g., scaling BDI for interpretability).

## Tools & Libraries
• Python
• Pandas
• NumPy
• Matplotlib
• Seaborn
• Statsmodels (OLS Regression)

## Methodology
1) Data Cleaning & Preparation
   - Verified headers and corrected formatting issues
   - Converted numeric columns from text to numeric types
   - Created scaled variables (e.g., BDI_k = BDI / 1000) for easier coefficient interpretation
   - Removed missing values in key fields used for modeling

2) Exploratory Data Analysis (EDA)
   - Summary statistics for all variables
   - Histogram of Price
   - Scatter plots of Price vs predictors
   - Correlation matrix heatmap
   - Scatterplot matrix

3) Regression Modeling
   - Simple Regression: Price = β0 + β1(Age) + ε
   - Multiple Regression: Price = β0 + β1(Age) + β2(DWT) + β3(BDI) + ε

4) Model Diagnostics & Validation
   - Residual vs fitted plots
   - Histogram and QQ plot of residuals
   - Cook’s distance / influence plot

5) Valuation & Scenario Analysis (Bet Performer)
   - Point prediction and uncertainty ranges
   - Scenario testing for age, DWT, and charter market conditions

## Key Insights
• Age has a strong negative relationship with price (depreciation)
• Larger ships (higher DWT) command higher prices
• BDI (charter market strength) significantly impacts ship prices
• Multiple regression provides higher predictive accuracy than age-only regression

## Results Summary
• Multiple regression achieved strong explanatory power (R² ≈ 0.92)
• Predictors Age, DWT, and BDI were statistically significant
• Prediction intervals highlighted realistic transaction uncertainty
• Scenario analysis strengthened valuation credibility

## Files in Repository
• Doha_Zaky_Final_Case_Study.ipynb — complete analysis notebook (along with the charts and regression analysis and diagnostics)
• sales.xlsx — dataset used for analysis

## How to Run
1. Clone the repository
2. Install dependencies: pandas, numpy, matplotlib, seaborn, statsmodels
3. Open the notebook and run all cells

## Author for the Case Study Regression Analysis 
Doha Zaky
MS in Data Science & Artificial Intelligence - Bryant University 
LinkedIn: https://linkedin.com/in/doha-zaky

## License
This project is for academic and portfolio purposes.
