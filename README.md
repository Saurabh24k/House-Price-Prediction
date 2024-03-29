# House Price Prediction Project

## Project Overview
This project is focused on predicting house prices using a comprehensive dataset reflecting various attributes of houses in California. Our approach integrates in-depth data exploration, rigorous preprocessing, feature engineering, and the deployment of machine learning models, followed by meticulous hyperparameter tuning to refine our predictions.

## Dataset
The dataset, named `housing.csv`, encompasses a diverse range of features including the number of rooms, bedrooms, population, households, latitude, longitude, median income, and ocean proximity, alongside the target variable of median house value. An initial exploration was undertaken to assess data quality, distribution, and potential correlations between features.

## Data Preprocessing and Exploration
### Initial Exploration
- **Missing Values**: Identified and removed rows with missing data to maintain data integrity.
- **Data Visualization**: Initial histograms and scatter plots were generated for each feature to understand the distributions and identify potential outliers. A geographical scatter plot of house values provided insights into regional price distributions.

![Histogram](https://github.com/Saurabh24k/House-Price-Prediction/blob/main/Hist.png "Histogram")


### Feature Engineering
- **Log Transformation**: Applied to `total_rooms`, `total_bedrooms`, `population`, and `households` to normalize their distributions, addressing observed skewness.
- **New Features**: Created `bedroom_ratio` and `household_rooms` to explore new dimensions of the data that might influence house prices.

### Visualization and Correlation Analysis
- **Histograms**: Before and after log transformation, histograms revealed significant improvements in the distribution of features, making them more symmetrical and less skewed.
- **Heatmaps**: Correlation heatmaps were crucial at multiple stages:
  - **Pre-Feature Engineering**: The initial heatmap helped identify strong and weak correlations between features and the target variable, guiding the feature engineering process.
   ![Pre Feature Enginnering](https://github.com/Saurabh24k/House-Price-Prediction/blob/main/Pre.png "Pre Feature Enginnering Heatmap")
  - **Post-Feature Engineering**: A subsequent heatmap provided a comparative view, showcasing the impact of newly engineered features and transformations on the correlations. Notably, the introduction of `bedroom_ratio` and `household_rooms` altered the correlation landscape, indicating their potential predictive power.
   ![Post Feature Enginnering](https://github.com/Saurabh24k/House-Price-Prediction/blob/main/PostFetEng.png "Post Feature Enginnering Heatmap")
- **Geographical Scatter Plot**: Enhanced with `palette="coolwarm"`, it visualized the relationship between location and house price, highlighting the price variance across regions.
   ![Geographical Scatter Plot](https://github.com/Saurabh24k/House-Price-Prediction/blob/main/Scatt.png "Geographical Scatter Plot")

## Modeling and Evaluation
Two primary models were deployed to predict house prices: Linear Regression and Random Forest Regressor.

### Linear Regression
- Served as the baseline for comparison.
- Evaluation before and after feature scaling demonstrated the importance of standardization in linear models.
- Accuracy - 67%

### Random Forest Regressor
- Selected for its robustness to outliers and capability to model complex, non-linear relationships.
- Showed superior performance to Linear Regression, emphasizing its efficacy in capturing the nuances of the dataset.
- Accuracy - 97%

### Hyperparameter Tuning
- Utilized `GridSearchCV` for the Random Forest model, exploring parameters such as `n_estimators`, `min_samples_split`, and `max_depth`.
- The optimal model configuration still the results or Random Forest Regressor are better.
- Accuracy - 96%

## Results and Comparison
- **Model Performance**: The Random Forest Regressor, especially after hyperparameter tuning, markedly outperformed the Linear Regression model, showcasing the value of model complexity and tuning in predictive accuracy.
- **Feature Engineering Impact**: The adjustments and additions to the feature set not only improved model performance but also provided deeper insights into the data through enhanced visualizations and correlation analysis.

## Conclusions and Learnings
- **Feature Engineering**: Critical in unearthing the underlying patterns within the dataset, leading to more accurate predictions.
- **Model Selection and Tuning**: The choice of model and subsequent tuning are pivotal in leveraging the dataset's characteristics to improve predictive performance.
- **Visualization**: A powerful tool for both initial exploration and ongoing analysis, aiding in understanding data transformations and correlations.

