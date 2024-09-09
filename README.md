# Predicting Hazardous Near-Earth Objects (NEOs)

## Project Overview

This project aims to predict whether a Near-Earth Object (NEO) is hazardous or not based on its characteristics. The dataset used in this project contains various features related to NEOs, such as their absolute magnitude, estimated diameter, and orbiting body. The target variable is a binary indicator of whether the NEO is considered hazardous.

The project follows a structured data science process, including data importing, cleaning, exploratory data analysis (EDA), data preprocessing, and model training and evaluation. Various machine learning models are trained and compared to identify the best-performing model for this classification task.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Approach](#approach)
  - [1. Data Importing and Cleaning](#1-data-importing-and-cleaning)
  - [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
  - [3. Data Preprocessing](#3-data-preprocessing)
  - [4. Model Training and Evaluation](#4-model-training-and-evaluation)
- [Key Findings](#key-findings)
- [How to Run](#how-to-run)
- [Conclusion](#conclusion)
- [Future Work](#future-work)

## Dataset

The dataset used in this project contains information on various NEOs. The features include:

- **absolute_magnitude**: The absolute magnitude of the NEO.
- **estimated_diameter_min**: The minimum estimated diameter of the NEO.
- **estimated_diameter_max**: The maximum estimated diameter of the NEO.
- **orbiting_body**: The celestial body that the NEO is orbiting.
- **is_hazardous**: A binary indicator (0 or 1) of whether the NEO is hazardous.

The dataset was cleaned and preprocessed to handle missing values, encode categorical variables, and standardize numerical features.

## Project Structure

- `Predicting Hazardous NEOs.ipynb`: The main Jupyter notebook containing the code for data cleaning, EDA, data preprocessing, and model training.
- `README.md`: The file you are currently reading, summarizing the project and providing instructions on how to use the code.

## Approach

### 1. Data Importing and Cleaning

- **Data Importing**: The dataset is imported using Pandas, and initial exploration is done to understand its structure.
- **Handling Missing Values**: Missing values in numerical columns were filled with the mean of the respective columns to maintain data integrity.
- **Duplicate Check**: The dataset was checked for duplicate rows, and none were found.

### 2. Exploratory Data Analysis (EDA)

- **Distribution of Target Variable**: The distribution of the `is_hazardous` column was visualized using a count plot to understand the class imbalance.
- **Feature Distribution**: The distribution of `absolute_magnitude` was visualized to gain insights into the range and skewness of this feature.
- **Correlation Analysis**: A correlation matrix was plotted to identify relationships between features and the target variable.
- **Scatter Plot Analysis**: A scatter plot was used to visualize the relationship between `estimated_diameter_max` and `absolute_magnitude`, colored by the `is_hazardous` indicator.

### 3. Data Preprocessing

- **Encoding**: The `orbiting_body` column was encoded using Label Encoding to convert categorical data into numerical format.
- **Feature Selection**: Irrelevant features (`neo_id`, `name`) were dropped from the dataset.
- **Data Splitting**: The data was split into training and testing sets (70/30) to evaluate model performance.
- **Standardization**: Numerical features were standardized using StandardScaler to ensure that they have a mean of 0 and a standard deviation of 1.

### 4. Model Training and Evaluation

Three machine learning models were trained and evaluated:

- **Random Forest Classifier**
- **Logistic Regression**


The models were evaluated using accuracy, precision, recall, F1-score, and ROC-AUC curves. The accuracy of each model was calculated and compared to determine the best-performing model.

## Key Findings

- The **Random Forest** model showed strong performance in terms of accuracy and was effective in predicting hazardous NEOs.
- The dataset is imbalanced, with fewer hazardous objects compared to non-hazardous ones, which was addressed during the modeling phase.

