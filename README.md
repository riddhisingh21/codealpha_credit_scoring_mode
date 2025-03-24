# Credit Scoring Model

## Overview:
  This project aims to develop a predictive model for assessing credit risk using a dataset containing various financial and demographic features. The goal is to accurately predict whether an individual will 
  default on their credit obligations, as indicated by the target variable DEFAULT (1 represents a default, and 0 represents no default).

## Dataset:
  The dataset includes several features related to customer demographics, income, savings, debt levels, and other financial indicators. It is preprocessed to handle missing values and ensure suitability for model 
  training.

## Methodology 
  3.1 Data Preprocessing 
      3.1.1 Handling Missing Values No missing values remain in the dataset after preprocessing.
            Numeric columns: Filled with their median values.
            Categorical columns: Filled with their mode values.
      3.1.2 Feature Selection Features are selected based on their relevance to predicting credit defaults, while irrelevant columns like CUST_ID are excluded.

  3.2 Data Visualization 
      3.2.1 Target Variable Distribution Visualizations are created to understand the distribution of the target variable DEFAULT, helping to identify class imbalance.
      3.2.2 Correlation Heatmap A heatmap is generated to visualize correlations between numerical features, aiding in feature selection and understanding relationships.

  3.3 Addressing Class Imbalance Due to the inherent class imbalance in credit default datasets (fewer defaults than non-defaults), SMOTE (Synthetic Minority Over-sampling Technique) is applied to oversample the 
  minority class, ensuring balanced training data.

  3.4 Model Selection and Training 
      3.4.1 Model Choice A Random Forest Classifier is chosen for its robustness and ability to handle complex patterns in the data.
      3.4.2 Hyperparameter Tuning Grid Search Cross-Validation (GridSearchCV) is employed to optimize the following hyperparameters:
            Number of estimators (n_estimators)
            Maximum depth of trees (max_depth)
            Minimum samples required to split an internal node (min_samples_split)
            Minimum samples required at a leaf node (min_samples_leaf)

  3.5 Model Evaluation The performance of the model is evaluated using:
      Accuracy Score: Measures the proportion of correctly classified instances.
      Confusion Matrix: Provides insights into true positives, true negatives, false positives, and false negatives.
      Classification Report: Includes precision, recall, and F1-score for both classes.
      ROC AUC Score: Assesses the model's ability to distinguish between classes.
      3.6 Results Visualization Visualizations such as confusion matrix heatmaps and ROC curves are generated to illustrate model performance visually.

## Conclusion:
  The final model demonstrates a balanced approach to predicting credit defaults with improved accuracy and recall for the minority class. This is achieved after implementing advanced techniques like 
  SMOTE and hyperparameter tuning. The insights gained from this analysis can be invaluable for financial institutions in assessing credit risk more effectively.
