# **Long-Term Growth Trends in the S&P 500 Index**

**Author:** Tahity Abdullah
**Course:** BSAN 360 – Final Project
**Date:** December 4, 2025

This repository contains the full analysis, code, and presentation for the project **“Long-Term Growth Trends in the S&P 500 Index.”** The goal of this project is to examine how the S&P 500 has grown over nearly a century, determine whether its long-term trend is statistically significant, and evaluate whether decade-level differences reveal meaningful market patterns.

## **Repository Contents**

### **1. Project Notebook**

`Project6.ipynb`
Contains all data preparation, exploratory analysis, hypothesis testing, and visualizations used in the project.
Includes:

* Data loading and cleaning
* Time-series transformations
* Regression modeling
* ANOVA testing
* Figures used in the final slide deck

### **2. Presentation Slides**

`Long Term Growth Trends in the S&P500 Index Presentation.pptx` 
Managerial-style slide deck summarizing the dataset, research questions, methods, key findings, and recommendations.

## **Dataset Information**

* **Source:** Kaggle – *S&P 500 Historical Data*
* **Date Range:** 1927–2024
* **Raw Size:** ~23,323 daily observations
* **Key Variables:** Date, Open, Close, Adj Close, Volume
* **Primary Analysis Variable:** *Adjusted Closing Price*

  * Reflects true market value
  * Accounts for stock splits and dividends

## **Data Cleaning & Preparation**

The notebook prepares a fully continuous daily time series by:

* Creating decade and year grouping variables
* Log-transforming adjusted close values to model exponential growth
* Removing missing or corrupted observations

**Final dataset includes:**

* 35,000+ daily rows
* Variables: `Adj Close`, `Year`, `Decade`, `Log_Close`
* No missing values in analysis variables

## **Research Question**

**How has the long-term growth rate of the S&P 500 evolved over time, and do annual or decade-level patterns reveal significant differences in market performance?**

## **Hypotheses**

### **1. Regression: Long-Term Trend**

* **H₀:** No relationship between time and log-adjusted closing price
* **H₁:** A significant positive long-term trend exists

### **2. ANOVA: Decade-Level Differences**

* **H₀:** Mean adjusted closing price is equal across all decades
* **H₁:** At least one decade differs significantly

## **Key Findings**

### **Regression**

* Strong, statistically significant upward trend in log-price
* Supports long-term exponential growth pattern

### **ANOVA**

* Decades differ significantly in mean price levels
* Confirms structural changes in market behavior over time

### **Visual Insights**

* Clear disruptions during major economic events (1930s, 2000s, 2008, 2020)
* Rising volatility in recent decades
* Annual returns are noisy, reinforcing importance of long-term analysis

## **Conclusions**

* The S&P 500 grows *exponentially* over long horizons.
* Short-term volatility does not disrupt the long-run upward trajectory.
* Market structure varies by decade, reflecting macroeconomic cycles.
* Long-term investors benefit more from buy-and-hold strategies than short-term timing.

## **How to Run the Notebook**

1. Clone the repository
2. Install required Python packages (pandas, numpy, matplotlib, statsmodels)
3. Run `Project6.ipynb` in Jupyter

