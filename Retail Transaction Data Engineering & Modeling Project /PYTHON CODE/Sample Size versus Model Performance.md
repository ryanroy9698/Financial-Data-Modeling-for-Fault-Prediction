# Part 3 Model Performance Comparison Based on Sample Size

## Factors Influencing Model Performance
1. Separation of classes: Examining whether classes are easily separated, linearly or non-linearly, and the type of model used.
2. Features quality: Assessing the informativeness of features in relation to the output/class.
3. Number of data points: Investigating the impact of dataset size on model performance.

## Dataset Size vs. Model Performance
To quantify the dataset size's influence on model performance, the best single tree model created in Part 3 was evaluated using datasets of varying sizes. Monthly_features were utilized for this analysis.

### Evaluation Steps:
1. The train/test sets were split with a 9:1 ratio, resulting in approximately 291k/32k samples in the train/test set.
2. A for loop was created to build and evaluate the tree model with different sample sizes (e.g., 50), repeating the process 10 times to calculate the mean and standard deviation of the test set AUC.
3. The procedure was repeated for different sample sizes (e.g., 100, 500, 1000, 2000, 5000, 10000).
4. A table was built containing:
   - Sample size (N)
   - Test AUC mean
   - Test AUC standard deviation
5. The `errorbar` function from Matplotlib was used to plot the model performance (test AUC mean and standard deviation) against the sample size. This plot aimed to estimate the minimum number of samples required for adequate modeling.

This analysis provided insights into the dataset size needed for accurate model performance in scenarios where collecting extensive post-event data is challenging.
