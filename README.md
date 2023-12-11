# Leveraging-machine-learning-algorithms-for-effective-permit-management

### Project Overview
The project used different machine learning algorithms to predict the amount of money to be paid by companies seeking to import certain chemicals into the country 
by applying for an import permit from one of Ghana's regulatory agencies.

This was done to:
- Ensure that monetary loss to the Commission resulting from mistakes made by manually calculating figures was resolved.
- Improve efficiency for the entire permit management process. 

### Dataset
The dataset was sourced from the regulatory agency. The names of the actual companies were however not included in the analysis. The dataset included the
following variables: 
- Date Prepared
- Chemical Name
- Quantity
- Unit (Kg/L)
- Permit Type
- Permit Number 
- Amount Paid (Target feature) 
- Date Issued

### Tool
- Python

### Data Cleaning
Data cleaning was done as the first step by removing some unwanted variables as well as missing values. 

### Data Exploration
The goal of data exploration is to get some insights by running an exploratory study on the data. Some specific tasks undertaken in this section included the attempt to comprehend the distribution of some variables, correlations, and potential insights regarding the relationship between 'Amount paid' being the
target variable and other varaibles or features. 

### Data Preprocessing
For the preprocessing stage, the following tasks were carried out:
- Observation of outliers
- Normalization
- Encoding
- Feature selection

### Modelling
#### Train and Test splits 
After completing data pre-processing, the next stage was to build different models. The data was now split into training and testing data using a ratio of 80% training data and 20% testing data.

### Models
The goal of the models created was to calculate the cost of the permits issued by the Commission based on a number of variables. The objective of this study is money, which is a continuous variable, thus the models to be used are all regression-based algorithms.
Several algorithms were tested namely: Multiple linear Regressor, Decision Tree Regressor, Random Forest Regressor, and Gradient Boosting Regressor
Each model underwent evaluation through metrics such as Mean Squared Error, R-squared, and Mean Absolute Error. Cross-validation techniques were also applied to ensure the models' robustness and generalizability

#### Multiple Linear Regression
Multiple Linear Regression (MLR) is a widely used statistical method in data analysis and predictive modeling, which allows an understanding of the relationship between a dependent variable and two or more independent variables. Multiple Linear Regression extends simple linear regression by accommodating multiple predictors (independent variables) to model the outcome of a dependent variable

##### Discussion
The linear regression model shows a substantial improvement in performance after the logarithmic transformation of the "Quantity" and "Amount paid" variables. The R-squared value increased significantly from 0.449 to 0.788. Cross-validation achieved a score of 72.9, suggesting that the model generalizes well to new data.

