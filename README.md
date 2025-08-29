## Food Delivery Time Prediction

### Project Overview

This project aims to predict the **delivery time for food orders** based on various factors that influence the delivery process. By analyzing features such as distance, weather, traffic, time of day, vehicle type, and preparation time, the goal is to develop a regression model that can accurately estimate the delivery duration. This is a critical task for food delivery services to improve logistics and customer satisfaction.

-----

### Technical Highlights

  * **Dataset**: The dataset used is `Food_Delivery_Times.csv`, which contains information about 1000 food delivery orders.
  * **Size**: 1000 entries, 9 columns.
  * **Key Features**:
      * **Order Details**: `Distance_km`, `Preparation_Time_min`.
      * **Environmental Factors**: `Weather`, `Traffic_Level`, `Time_of_Day`.
      * **Courier Info**: `Vehicle_Type`, `Courier_Experience_yrs`.
  * **Approach**:
      * **Data Cleaning**: Rows with missing values in `Weather`, `Traffic_Level`, `Time_of_Day`, and `Courier_Experience_yrs` were handled. Outliers in the target variable `Delivery_Time_min` were removed using the IQR method. The `Order_ID` column was dropped.
      * **Exploratory Data Analysis**: Histograms, box plots, count plots, and scatter plots were used for visualization to understand data distributions and feature relationships.
      * **Categorical Encoding**: Categorical features were encoded using `LabelEncoder`.
      * **Regression Task**: The target variable is `Delivery_Time_min`.
      * **Models Used**:
          * A suite of regression models were trained, including Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN). Missing values were imputed using `SimpleImputer` within a `Pipeline`.
  * **Best R² Score**:
      * **0.817** with Ridge and Gradient Boosting Regressors.
      * **0.809** with XGBoost Regressor.
      * **0.789** with KNN Regressor.
      * The scatter plots show a good fit between actual and predicted values, indicating that the models are effective at predicting delivery times.

-----

### Purpose and Applications

  * Enable food delivery companies to **provide accurate Estimated Time of Arrival (ETA)** to customers.
  * Optimize courier dispatching and routing to minimize delivery times.
  * Improve customer satisfaction and retention by setting realistic delivery expectations.
  * Support data-driven decision-making in logistics and operational management.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Food-Delivery-Time-Prediction-Using-ML.git
cd Food-Delivery-Time-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning for the top-performing regression models.
  * Exploring more advanced feature engineering, such as combining `Distance_km` with `Courier_Experience_yrs` to create a `speed` feature.
  * Investigating the impact of the data cleaning and encoding steps, and trying alternative methods.
  * Adding explainability (e.g., SHAP or LIME) to understand which factors are the most significant drivers of delivery time.
