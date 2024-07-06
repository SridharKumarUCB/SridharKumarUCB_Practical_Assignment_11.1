# SridharKumarUCB_Practical_Assignment_11.1

### PROBLEM STATEMENT:
Our business objective is to identify key determinants influencing used car prices. This includes transforming the business obective into a data mining task that analyzes various features such as model, condition, mileage, year manufactored, and others. The goal is to leverage the data mining techniques to disover any patterns or relationships that affect such variations in car price. By identifying these factors, we aim to develop predictive models that can estimate the prices of used cars based on their attributes.

### DATA Understanding:

The first step was to understand the dataset and explore what information it contains, and how this could be used to inform better business understanding. The steps involved were:

1. Load Data
2. Preview Data
3. Assess the data
4. Check for null values
5. Exploratory Data Analysis (EDA)

From this section we understood that the dataset consisted mostly of categories. Also, a lot of columns had an excessive amount null values and inconsistencies. Some early correlations seen were the correlation between transmission and fuel, and the correlation between paint color and car type. We also saw that newer cars sold for higher, which makes sense. Conditions of the used car was also an important factor; cares that were 'like new' or 'excellent', on average, sold for higher. 

### DATA ANALYSIS FINDINGS:

We used multiple regression models and tested them to accurately predict car prices. These models included, Linear, Ridge, Lasso, and Elastic Net regression models. Our analysis indicates that Elastic Net Regression is most suitable model for predicting used car prices for inventory management needs.

A high quality model should have results where the RMSE is low and R2 is highest. Our models before minimizing the dataset showed an RMSE value of around 19786236.8919 and R2 to be -0.0001. This suggests that the model has severe issues. This prompted us to refine our approach by focusing on a subset of the dataset, leading to significant improvement. By minimizing the dataset, we determined that Ridge Regression to be the best model before cross-validation. Our ridge regression model resulted in an RMSE score of 9170.9563 and an R2 value of 0.5547. A 0.5547 R2 value suggests that about 55% of the variance in the target variable is explained by the features in our model. This model is not that much better however, as we were expecting an RMSE score much lower ( < 10). After cross validation, all models show higher RMSE values on the test set compared to their cross-validation RMSE. This indicates over-fitting and generally bad performance. Ridge and Lasso regressions show a decrease in R2 on the test set compared to their cross-validation. Again, indicating bad performance. One interesting thing to note is that Elastic Net shows a slight improvement in R2 on the test set compared to cross-validation. This may suggest that it is better in generalizing to the unseen data. Ultimately, after cross-validation Elastic Net emerges as the best model even if further refinement is needed. Elastic Net had a RMSE score of 9238.5340 and an R2 value of 0.5481 (meaning that about 54.8% of the variance in the target variable is explained by the features in our model).

### Future Work

The challenges encountered, including dataset size, inconsistencies, and complexity, significantly impacted initial model performance. Moving forward, we intend to revisit our data preparation phase to address these issues more rigorously. This includes addressing data inconsistencies such as missing values and outliers, which we suspect contributed to suboptimal model outcomes (also revisiting feature engineering and considering additional features). We could even explore more complex models that could potentially capture the underlying patterns in the data more effectively. After further refinement of the model, it will be best suited to confidently assist in predicting car prices.

