# Credit-Card-Fraud-Classification
This notebook covers credit card fraud classification.

It's split into 5 sections:
1) Data preparation and interpretation
2) Data preprocessing
3) Exploratory data analysis
4) Machine learning classification
5) Neural network classification

This README covers the best methods used in this notebook, though more are covered.

##### Data preparation and interpretation
First the data is found to be extremely unbalanced like so:

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/1-1.png?raw=true "Data imbalance")

##### Data preprocessing
The data is balanced using SMOTE to achieve equal outcome.

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/1.png?raw=true "Balanced dataset SMOTE")

This has a great effect on the correlation between features and class, comparing the top correlation plot to the last.

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/2.png?raw=true "Correlation matrix")

Next the outliers are removed from the fraudulent datapoints to increase model accuracy.
Before:

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/3.png?raw=true "Data with outliers")

After:

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/4.png?raw=true "Data outliers removed")

##### Exploratory data analysis
Features of the data are explored, startin with higher order correlations

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/5.png?raw=true "Higer order correlations")

Revealing some quadratic relationships to be tested with models later on.
Next the data is dimensionally reduced and plotted to see differentiation between fraud and non-fraud cases
Features of the data are explored, startin with higher order correlations

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/6.png?raw=true "Data plots")

##### Machine learning classification
NOTE: Since the data is now equally distributed between classes, the standard accuracy metric is perfectly acceptable (this is not the case for imbalanced datasets).

The data is modelled and the best outcome KNN at 99.87% is graphed showing a nice result, all fraudulent cases are correctly classified.

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/7.png?raw=true "KNN confusion matrix")

The KNN model being the best predicter is then optimised increasing the accuracy to 99.96%

![Alt text](https://github.com/MattH96/Credit-Card-Fraud-Classification/blob/master/Images/8.png?raw=true "KNN optimised confusion matrix")

##### Neural network classification
A neural network model is created, care has been taken to make the model complex enough to distinguish the large and varied dataset produced, I found underfitting easy to achieve.
