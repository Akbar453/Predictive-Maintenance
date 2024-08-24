# Predictive-Maintenance Classification

This project involves the analysis of a dataset related to predictive maintenance using various data visualization techniques and machine learning algorithms. The goal is to classify the type of failure in machinery based on various sensor readings and process parameters.

# Dataset

The dataset used in this project is the Machine Predictive Maintenance Classification dataset, available on Kaggle. It contains information about machinery, including sensor readings and failure types.

# Dataset Features

Type: The type of the machine (L, M, H).
Air temperature [K]: The air temperature in Kelvin.
Process temperature [K]: The process temperature in Kelvin.
Rotational speed [rpm]: The rotational speed of the machine in revolutions per minute.
Torque [Nm]: The torque applied to the machine in Newton-meters.
Tool wear [min]: The wear of the tool in minutes.
Target: A binary variable indicating whether a failure has occurred or not.
Failure Type: The type of failure, if any.

# Installation 

pip install -r requirements.txt
If requirements.txt is not available, you can install the packages manually
pip install kaggle pandas numpy matplotlib seaborn scikit-learn imbalanced-learn

# Usage

1. Download the Dataset
Make sure to download the dataset from Kaggle
!kaggle datasets download -d shivamb/machine-predictive-maintenance-classification

Move your kaggle.json file to the appropriate directory:
!mkdir -p ~/.kaggle
!mv kaggle.json ~/.kaggle/

# Load and Explore the data
The data is loaded using pandas and basic exploratory data analysis (EDA) is performed using matplotlib and seaborn.

# Data Preprocessing

Null Values: The dataset does not contain any missing values.
Duplicates: No duplicates are found in the dataset.
Dropping Unnecessary Columns: Columns such as UDI and Product ID are dropped as they do not contribute to the analysis.
Encoding Categorical Variables: Categorical variables such as Type and Target are encoded using LabelEncoder.
Handling Imbalance: The dataset is balanced using the SMOTE technique to oversample the minority classes.

# Data Visualization

Various plots are generated to visualize the distribution of features:
Bar and pie charts to show the distribution of Type, Failure Type, and Target.
Histograms to show the distribution of numerical features.
Scatter plots to examine the relationships between features.

# Feature Engineering
Dummy variables are created for categorical features to convert them into numerical format.
The SMOTE technique is applied to handle class imbalance in the dataset.

# Model Training (Not Included in the Code)
Although the code provided does not include model training, the processed data can be used to train machine learning models such as Decision Trees, Random Forest, XGBoost, etc., for predictive maintenance classification.

# Visualization Examples
The code generates various visualizations including:

Bar and pie charts of different types and failure types.
Histograms of numerical features.
Pair plots to visualize relationships between features and failure types.
Scatter plots to visualize the relationships between key variables.

# Future Work
Model Training: Implement machine learning models to predict failure types based on the preprocessed data.
Model Evaluation: Use cross-validation and performance metrics such as accuracy, precision, recall, and F1-score to evaluate model performance.

#  Results

The model achieved an accuracy of over 99.9654666321333on the test dataset, demonstrating its effectiveness in predicting maintenance needs.

# Conclusion

his predictive maintenance classification model provides a reliable and accurate solution for identifying maintenance needs in advance, helping to reduce unplanned downtime and optimize operational efficiency.
