# Near-Earth Object Hazard Prediction

Machine learning classification of potentially hazardous Near-Earth Objects (NEOs) using NASA observational data.

## Project Overview

This project applies machine learning classification techniques to predict whether a Near-Earth Object is potentially hazardous based on its observed physical and orbital characteristics.

The project includes data preprocessing, exploratory data analysis, feature transformation, machine learning model development, and model evaluation.

## Dataset

The project uses a Near-Earth Object dataset containing observational and orbital characteristics of NEOs.

The dataset includes features such as:

- Estimated minimum diameter
- Estimated maximum diameter
- Relative velocity
- Miss distance
- Absolute magnitude
- Orbiting body
- Hazardous classification

The target variable is:

- `hazardous` — indicates whether the object is classified as potentially hazardous.

## Data Preprocessing

The following preprocessing steps were implemented:

- Handled missing numerical values using median imputation.
- Handled missing categorical values using an `Unknown` category.
- Converted the hazardous target variable into numerical form.
- Standardized numerical features using `StandardScaler`.
- Applied one-hot encoding to categorical features.
- Removed non-essential columns such as object ID, name, and Sentry object information.

## Exploratory Data Analysis

The project includes several visualizations to investigate relationships between NEO characteristics and hazardous classification.

Visualizations include:

- Correlation heatmap
- Relative velocity vs. hazardous status boxplot
- Miss distance vs. hazardous status boxplot
- Absolute magnitude distribution by hazardous status

The exploratory analysis indicated relationships between hazardous classification and characteristics such as miss distance, absolute magnitude, and relative velocity.

## Machine Learning Models

The project implemented and evaluated the following classification models:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

Class balancing was incorporated for Logistic Regression and Random Forest using `class_weight='balanced'` to address the imbalance between hazardous and non-hazardous objects.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Classification report
- Confusion matrix

The project uses an 80/20 train-test split with a fixed random state for reproducibility.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
near-earth-object-hazard-prediction/
│
├── NEO_Hazard_Prediction.ipynb
├── README.md
└── requirements.txt
