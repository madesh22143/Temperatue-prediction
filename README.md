Temperature Prediction Using Machine Learning
1. Introduction

Temperature prediction is an important task in weather forecasting, agriculture, environmental monitoring, and climate analysis. By analyzing historical weather data such as humidity, temperature trends can be estimated using machine learning techniques.

Machine Learning allows computers to learn patterns from historical data and make predictions on unseen data. In this project, a Linear Regression model is used to predict temperature based on humidity values.

Humidity and temperature are closely related atmospheric variables. Generally, when humidity increases, the perceived temperature may change due to moisture content in the air. Therefore, analyzing this relationship helps build predictive models.

2. Objective of the Project

The main objective of this project is:

To analyze the relationship between humidity and temperature

To perform Exploratory Data Analysis (EDA) on the dataset

To build a machine learning model that predicts temperature

To evaluate the model performance using regression metrics

3. Dataset Overview

The dataset used in this project contains environmental readings including:

Feature	Description
Temperature	The atmospheric temperature value
Humidity	The amount of water vapor present in air

The dataset may contain hourly or daily measurements collected from weather monitoring systems.

Before building the model, the dataset must be explored to understand:

Data types

Missing values

Statistical properties

Relationship between variables

4. Exploratory Data Analysis (EDA)

Exploratory Data Analysis is an important step in any data science project. It helps understand patterns, detect anomalies, and identify relationships between variables.

Steps performed in EDA
1. Checking dataset information

Using functions like:

df.info()

df.head()

These help understand:

Number of rows and columns

Data types

Sample values

2. Summary Statistics

Summary statistics provide information such as:

Mean

Median

Standard deviation

Minimum and maximum values

This is obtained using:

df.describe()

These statistics help understand the distribution and spread of the data.

3. Missing Value Detection

Missing values can negatively impact model performance. Therefore they must be handled properly.

df.isnull()

If missing values exist, they can be:

Removed

Replaced with mean/median values

In this project, rows containing missing values are removed.

5. Data Visualization

Data visualization helps understand relationships between variables.

Scatter Plot

A scatter plot is used to visualize the relationship between humidity and temperature.

plt.scatter(temperature, humidity)

The scatter plot helps determine:

Whether the relationship is linear

Whether there are outliers

The direction of correlation

If the points follow a linear trend, then Linear Regression is suitable.

6. Data Preprocessing

Before training a machine learning model, the dataset must be prepared.

Feature and Target Variables

In machine learning:

Feature (X) → Input variable

Target (y) → Output variable

In this project:

Feature:

Temperature

Target:

Humidity

The feature is used by the model to predict the target variable.

7. Train-Test Split

To evaluate the performance of the model, the dataset is divided into two parts:

Dataset	Purpose
Training Data	Used to train the model
Testing Data	Used to evaluate the model

Typical split:

80% Training Data

20% Testing Data

This is done using:

train_test_split()

This ensures the model is tested on unseen data.

8. Machine Learning Model – Linear Regression
What is Linear Regression?

Linear Regression is a supervised learning algorithm used for predicting continuous values.

It finds the best-fit straight line that represents the relationship between variables.

The mathematical equation is:

𝑦
=
𝑚
𝑥
+
𝑐
y=mx+c

Where:

y → predicted value

x → input feature

m → slope of the line

c → intercept

The algorithm tries to minimize prediction error and find the line that best fits the data.

9. Model Training

The Linear Regression model is trained using the training dataset.

Steps:

Import the model from sklearn

Fit the model with training data

Learn relationship between temperature and humidity

During training, the model learns the mathematical relationship between variables.

10. Model Prediction

After training, the model is used to make predictions on the test dataset.

y_pred = model.predict(X_test)

These predictions are then compared with actual values to evaluate performance.

11. Model Evaluation

To measure how well the model performs, evaluation metrics are used.

1. Mean Absolute Error (MAE)

Measures the average absolute difference between predicted and actual values.

Formula:

𝑀
𝐴
𝐸
=
1
𝑛
∑
∣
𝑦
−
𝑦
𝑝
𝑟
𝑒
𝑑
∣
MAE=
n
1
	​

∑∣y−y
pred
	​

∣

Lower MAE indicates better performance.

2. Mean Squared Error (MSE)

Measures the average squared difference between predicted and actual values.

𝑀
𝑆
𝐸
=
1
𝑛
∑
(
𝑦
−
𝑦
𝑝
𝑟
𝑒
𝑑
)
2
MSE=
n
1
	​

∑(y−y
pred
	​

)
2

It penalizes larger errors more strongly.

3. R² Score (Coefficient of Determination)

Measures how well the model explains the variance in the data.

Range:

0 → Poor model

1 → Perfect model

Higher R² means better predictive ability.

12. Advantages of Linear Regression

Simple and easy to understand

Fast to train

Works well for linear relationships

Provides interpretable results

13. Limitations

Cannot capture complex non-linear relationships

Sensitive to outliers

Requires assumptions such as linearity and independence

For more complex patterns, models like:

Polynomial Regression

Decision Trees

Random Forest

Neural Networks

can be used.

14. Conclusion

In this project, a Linear Regression model was implemented to predict temperature based on humidity data.

The process included:

Data loading

Exploratory Data Analysis

Data preprocessing

Model training

Model evaluation

