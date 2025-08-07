Titanic Survival Prediction Project
📜 Overview
This project analyzes a synthetic dataset of 1 million Titanic passengers to identify the key factors that influenced survival. The goal was to perform a comprehensive exploratory data analysis (EDA), uncover insights, and build a machine learning model to predict passenger survival.

📊 Dataset
The data used is the "Titanic Huge Dataset - 1M Passengers" from Kaggle. It is a synthetic but realistic dataset that preserves the statistical patterns of the original Titanic manifest while providing a large volume of data for analysis.

📋 Project Workflow
The analysis followed a structured data science workflow:

Problem Definition: Define the goal of the analysis and the key questions to explore.

Load & Inspect Data: Load the dataset using Pandas and perform an initial inspection to understand its structure, data types, and null values.

Data Cleaning: Handle missing values in the Age and Embarked columns, and drop columns (Cabin) with insufficient data.

Exploratory Data Analysis (EDA): Create visualizations to uncover trends, distributions, and relationships between different passenger attributes and survival.

Answering Key Questions: Use data groupings and plots to answer specific questions about survival factors.

Modeling: Build a simple Logistic Regression model to predict survival based on key features.

Summary: Document the key findings and model performance.

💡 Key Findings & Visualizations
The exploratory data analysis revealed several key factors that strongly correlated with a passenger's chance of survival.

Gender: Being female was the single most significant advantage for survival.

Passenger Class (Pclass): First-class passengers had a much higher survival rate than those in second and third class.

Age: Children had a higher survival rate than adults, especially those in first and second class.

🤖 Modeling and Results
A Logistic Regression classifier was trained using the following features: Pclass, Age, SibSp, Parch, Fare, Sex, and Embarked.

After training and testing the model on a 20% holdout set, the model achieved a final accuracy of:

Model Accuracy: 80.23%

This result indicates that passenger demographics and ticket information are strong predictors of survival.

🛠️ Tools Used
Language: Python

Libraries:

Pandas (Data Manipulation and Cleaning)

NumPy (Numerical Operations)

Seaborn & Matplotlib (Data Visualization)

Scikit-learn (Machine Learning Model)

Environment: Jupyter Notebook
