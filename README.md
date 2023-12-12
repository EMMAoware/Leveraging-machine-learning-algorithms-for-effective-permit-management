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

#### Multiple Linear Regression
The linear regression model shows a substantial improvement in performance after the logarithmic transformation of the "Quantity" and "Amount paid" variables. The R-squared value increased significantly from 0.449 to 0.788. Cross-validation achieved a score of 72.9, suggesting that the model generalizes well to new data.

#### Decision Tree
The decision tree regression model was initially configured with a maximum depth of three. The model achieved an R-squared value of 0.90. After hyperparameter
tuning, the optimum depth size for which the model was able to achieve its maximum accuracy was found to be 4 or higher. This resulted in an R-squared value of 0.98.

#### Random Forest 
The random forest regression model was initially configured with the number of trees or estimations set at ten. The model achieved an R-squared value of 0.986. After hyperparameter tuning, the optimum number of trees was found to be 150 for which the model recorded a slight improvement by recording and R-squared value of 0.9877.

#### Gradient Boost Regressor
The random boost regression model was initially configured with a max depth of 2, the number of trees or estimations set at three, and a learning rate of 1. An R-squared value of 0.892 was achieved. Hyperparameter tuning performed via GridSearchCV, aimed to search for the best combination of hyperparameters. The identified values were : max_depth = 4, n_estimators = 100, and learning_rate = 0.1 all resulted in a significantly improved R-squared score of 0.989.

### Conclusion
The high accuracy of predictions regarding the amount paid for permits enhances the Commission’s ability to anticipate and allocate resources effectively, facilitating better regulatory decision-making. Moreover, the insights gleaned from this model can potentially aid in the identification of anomalies or irregularities in the issuance of permits and enhance the overall effectiveness of the permit management process. 
