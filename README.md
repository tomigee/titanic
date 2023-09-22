# Learning from Disaster: Titanic Dataset
## Introduction
Can one predict the survival of passengers on the titanic based on attributes like their name, age, gender, title, ticket number, room number, the port they boarded from, etc.? In this project, I attempt to do just that. Kaggle provides datasets of passengers on the titanic from which our model will learn and on which our model will make predictions.

## Procedure
In this project, I trained and tested using a linear regression model, logistic regression model, and neural network. The data processing pipeline can be broken down into the following sections:
- Data Cleaning: Here I ensured that all numerical data is stored as numeric dtype, there are no missing values, and the training and testing dataset are appropriately separated. Some combination of the steps below were used in t
    - Dropping the `Cabin` column.
    - Drop rows with missing `Embarked` values.
    - Delete rows missing an `Age` entry, or mean impute `Age` values for rows where it's missing.
    - Deleting the `Name` column altogether, or extracting a `Prefix` feature from the `Name` column and then deleting it.
    - Deleting the `Ticket` column altogether, or extracting three categorical features from it and then deleting it.
    - Mean imputing missing values in the `Fare` column.
    - Deleting the `PassengerId` column since it's likely a unique identifier, or normalizing it and keeping it.
 - Encode categorical features: Transform all categorical features into numeric type.
 - Normalizing the dataset if needed.

## Results
The highest accuracy score was 0.778 and achieved with a Linear Regression Model.
