# Financial Giants Revenue Analysis

This project conducts an in-depth exploratory data analysis (EDA) of the top financial companies based on their revenue in 2024. The analysis includes visualizations and statistical techniques to uncover key trends and insights. We explore metrics like revenue, net income, total assets, and industry categorization. Additionally, we provide insights into geographical distribution, correlations between different metrics, and trends within the financial sector.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset Information](#dataset-information)
3. [Methodology](#methodology)
4. [Data Analysis and Visualizations](#data-analysis-and-visualizations)
   1. Top 10 Companies by Revenue
   2. Top 10 Companies by Net Income
   3. Top 10 Companies by Total Assets
   4. Distribution of Revenue, Net Income, and Total Assets
   5. Industry-Wise Aggregates
   6. Correlation Matrix
5. [Conclusion](#conclusion)
6. [Future Work](#future-work)

## Project Overview

In this project, we explore and analyze the financial data of the top 50 financial companies based on their revenue in 2024. The dataset includes columns such as:

- **Company**: Name of the financial company
- **Industry**: Type of industry (e.g., Banking, Insurance)
- **Revenue in (USD Million)**: Revenue in million USD
- **Net Income in (USD Million)**: Net income in million USD
- **Total Assets in (USD Million)**: Total assets in million USD
- **Headquarters**: Country of headquarters

The goal is to analyze the trends and patterns across multiple metrics, including revenue, net income, and assets.

## Dataset Information

The dataset used in this project is a CSV file titled `largest financial services companies by revenue`. It contains information on the top 50 financial companies by revenue for the year 2024. The dataset has the following columns:

- **Rank**: Rank of the company based on revenue
- **Company**: Company name
- **Industry**: Type of financial industry (e.g., banking, insurance)
- **Revenue in (USD Million)**: Revenue of the company in million USD
- **Net Income in (USD Million)**: Net income in million USD
- **Total Assets in (USD Million)**: Total assets in million USD
- **Headquarters**: Country where the company is based

## Methodology

The data analysis is performed using Python, utilizing the following libraries:

- **Pandas**: For data manipulation and analysis
- **Matplotlib**: For creating static visualizations
- **Seaborn**: For advanced visualizations
- **Plotly**: For interactive visualizations
- **NumPy**: For numerical operations

Key steps in the analysis include:

1. **Data Loading**: Loading the dataset into a pandas DataFrame.
2. **Data Exploration**: Investigating the structure, types, and summary statistics of the dataset.
3. **Data Visualization**: Creating a range of plots, such as bar charts, histograms, and correlation matrices.
4. **Data Aggregation**: Summarizing data by industry, revenue, net income, and assets.

## Data Analysis and Visualizations

### 1. Top 10 Companies by Revenue (USD Million)

The top 10 companies by revenue are visualized using a bar plot.

```python
top_revenue = df.nlargest(10, 'Revenue in (USD Million)')
sns.barplot(x=top_revenue['Revenue in (USD Million)'], y=top_revenue['Company'], palette='Blues_r')
