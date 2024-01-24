# Part 2: Predictive Modeling Using Annual and Monthly Trends: Feature Engineering and Machine Learning  
Two feature engineering approaches are considered: using annual features and monthly features. Three different algorithms are employed: Logistic Regression with L1 regularization, Decision Tree, and Random Forests.

### 1. Importing and Joining Data
- Imported annual and monthly features from tables generated in previous section.
  - annual_features
  - annual_day_of_week_counts_pivot
  - mth_rolling_features
  - mth_day_counts
  - days_since_last_txn
    
- Joined the features with the clients' responses from Retail_Data_Response.

### 2. Steps for Each Method
- **Annual Features:**
  - Separated inputs (X) and outputs (y).
  - Split data into train and test sets.
  - Pre-processed data if necessary.
  - Fit the training dataset, optimized hyperparameters, and plotted coefficient values or feature importance.
  - Plotted probability distribution for the test set.
  - Plotted confusion matrix and ROC curves, calculated precision/recall.
  - Plotted decision boundary for top 2 features.

- **Monthly Features:**
  - Repeated the same steps as with annual features.

### 3. Comparison of Methods
- Compared outcomes of step 2 for both feature engineering approaches and three modeling approaches.
- Selected the best combination for deployment in a production environment based on the comparison.
- Tabularized findings in step 2 to summarize results and support the decision.

## Findings and Decision
- Summarized findings from step 2 for each method.
- Selected the most effective combination of feature engineering and modeling approach for deployment in a production environment.
- Supported the decision with the provided tables and detailed results.

