# HOUSING PRICE PREDICTION of Ames, Iowa Dataset

![](/Images/external-content.duckduckgo.com.jpeg)

<u>**Workflow**</u>:

*  drop features with more missing values than actual values;

* Categorical Features:
  - Check class imbalance:
    - drop features with one category that represent more than 70%;
  - Impute missing values with "No_FeatureName", example: No Garage
  - One Hot Encoding 
* Numerical Features:
  - Check class imbalance to drop missing values with that are more representative than other cat
  - Impute missing values with 0
  - create new features: 
    * Total_Area: groud living area + total basement area
    * Total_Porch_Area
    * HalfBaths: total half baths
    * Full Baths: total full baths
  - check both correlation matrix and recursive feature elimination ranking to drop features that are redundant or highly correlated to each other
* Scaling
* Run the following model for predictions:
  * ElasticNet for regularization, search the best paramenters with GridSearch and then make predictions
  * GradientBoostingRegressor with Gridsearch to find the best parameters
  * XGBRegressor with GridSearch to find the best parameters



Still working on:

- using DNN and CNN1d
- improve predictions
- clean the code by wrapping up with functions