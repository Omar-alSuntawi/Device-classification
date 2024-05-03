﻿# Devices Price Classification System

## Technologies Used:
- Visual Studio Code
  
- Python
  - Flask
    
- Spring Boot 3.2.5
  - Spring Web Dependency
  - H2 Database
  - JPA Repository
    
- Machine Learning ( Sklearn )
  - Logistic Regression ( 4 Classes )

## Project Guide:
- Requirements:
1. Java 22 JDK
2. Maven 3.9.6
3. Flask
4. Sklearn

- Structure Description:
1. Python Folder:
  1. Omar_alSuntawi.ipynb --> Python Notebook in which several ML classifiers "Random Forest, KNN, Naive Bayes, Decision Trees, Logistic Regression, Support Vector Machine" were fitted to "train.csv" file after data preprocessing steps and EDA. In addition, performing hyper-parameters tuning using GridSearch to find the best tuning for each model. Finally, application of different assessments and metrics such as "Accuracy, Precision, Recall, F1 Score, and more"
  2. LR_best.pkl --> Pickle file in which the best model with the best hypertuning of parameters is selected and ready to be loaded on any test data.
  3. 
