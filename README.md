# Capstone Project: Walmart Sales Analysis and Forecasting

This project analyzes weekly sales data from Walmart's retail outlets to derive insights and predict future sales. It includes exploratory data analysis (EDA), statistical analysis, and predictive modeling using ARIMA.

## Project Overview

The dataset contains weekly sales information for various Walmart outlets, along with additional features such as temperature, fuel price, unemployment rate, and the Consumer Price Index (CPI). The goal of this project is to explore the factors that influence sales, identify patterns, and forecast future sales for better inventory management.

## Dataset

The dataset used for this analysis is `walmart.csv`, which contains 6435 rows and 8 columns. You can download the dataset from the following Kaggle link:

[Download Walmart Dataset](https://www.kaggle.com/datasets/yasserh/walmart-dataset)

### Dataset Features

| Feature Name        | Description                                               |
|---------------------|-----------------------------------------------------------|
| `Store`             | Store number                                              |
| `Date`              | Week of sales                                             |
| `Weekly_Sales`      | Sales for the given store in that week                    |
| `Holiday_Flag`      | Flag indicating if the week includes a holiday            |
| `Temperature`       | Temperature on the day of the sale                        |
| `Fuel_Price`        | Cost of fuel in the region                                |
| `CPI`               | Consumer Price Index                                      |
| `Unemployment`      | Unemployment rate in the region                           |

## Analysis

### 1. Data Preprocessing and Exploratory Data Analysis (EDA)

- **Missing Values:** The dataset is checked for missing values.
- **Box Plot for Weekly Sales:** A box plot visualizes the distribution of weekly sales, identifying potential outliers.

### 2. Key Insights

- **Unemployment Rate vs. Weekly Sales:** The correlation between unemployment and sales is analyzed to determine if there is a relationship.
- **Seasonal Trend Analysis:** The sales data is decomposed to identify seasonal patterns using `seasonal_decompose`.
- **Temperature vs. Weekly Sales:** A correlation is calculated to explore the impact of temperature on sales.
- **CPI vs. Weekly Sales:** The relationship between the Consumer Price Index and weekly sales is analyzed.
- **Top Performing Stores:** The top 10 stores with the highest total sales are identified.
- **Worst Performing Store:** The store with the lowest total sales is identified, and the difference between the highest and lowest performing stores is calculated.

### 3. Predictive Modeling

- **Data Preparation:** The date column is transformed into separate features for year, month, week, and day.
- **Train-Test Split:** The data is split into training (80%) and testing (20%) sets.
- **ARIMA Model:** An ARIMA model is used for forecasting future sales. The model is trained on the historical data and evaluated based on Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
- **12-Week Sales Forecast:** The model forecasts the sales for the next 12 weeks.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- sklearn

## Installation

To install the required libraries, run the following command:

```bash
pip install -r requirements.txt
