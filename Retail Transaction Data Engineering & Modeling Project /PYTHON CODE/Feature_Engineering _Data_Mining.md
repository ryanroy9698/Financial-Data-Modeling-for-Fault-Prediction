## Problem Description
The task is to predict clients' response to a promotion campaign, treating it as a classification problem with binary responses (0 for negative response, 1 for positive response). The features are derived from annual and monthly aggregations.

## Approach
Two feature engineering approaches are considered: using annual features and monthly features. Three different algorithms are employed: Logistic Regression with L1 regularization, Decision Tree, and Random Forests.

# Part 1: Feature Engineering Overview

## 1. Importing Data and Creating Anchor Date Columns
### 1.1 Importing and Data Transformation
- Imported transaction data as `txn1`.
- Transformed 'trans date' to 'txn date' using `pd.to_datetime`.
- Created 'ME DT' (last day of the month) and 'YEAR' columns.

## 2. Creating Features Capturing Annual Spending
### 1.2 Annual Features
- Utilized groupby and NamedAgg to create 'clnt_annual_aggregations'.
- Plotted histograms of sum and count.
- Reshaped the table using pivot_table, imputed NaN values.
- Saved the pivot table as 'annual features.xlsx'.
- Discussed possible disadvantages of annual features.

## 3. Creating Monthly Aggregations
### 1.3 Monthly Aggregations
- Created 'clnt_monthly_aggregations' capturing monthly sum and count.
- Plotted histograms.
- Explored common and maximum values.
- Saved the dataframe as 'mth day counts.xlsx'.

## 4. Creating Base Table for Rolling Window Features
### 1.4 Base Table
- Created a base table with all possible combinations of 'customer id' and 'ME DT'.
- Validated unique clients and month-end-dates.
  
## 5. Creating Monthly Rolling Window Features
### 1.5 Rolling Window Features
- Left-joined 'base_table' with 'clnt_monthly_aggregations'.
- Calculated 3, 6, and 12-month rolling window features.
- Merged tables and saved as 'mth rolling features.xlsx'.

## 6. Date-Related Features: Date of the Week
### 1.6 Date of the Week Features
- Extracted day of the week from 'txn date'.
- Created features capturing counts per client, year, and day of the week.
- Saved the annual pivot table as 'annual day of week counts pivot.xlsx'.
- Created features capturing counts per client, month-end-date, and day of the week.
- Joined with 'base_table' and saved as 'mth day counts.xlsx'.

## 7. Date-Related Features: Days Since Last Transaction
### 1.7 Days Since Last Transaction Features
- Created 'last_monthly_purchase' table capturing the last transaction date in each month.
- Joined with 'base_table' and forward-filled NaT values.
- Calculated 'days since last txn' and imputed remaining NaN values.
- Plotted a histogram and saved as 'days since last txn.xlsx'.

