# Cancer Mortality Rate Prediction Using Linear Regression and Deep Neural Networks

## Dataset Description - 

The data was aggregated from a number of sources including the American Community
Survey (https://www.census.gov), https://www.clinicaltrials.gov, and https://www.cancer.gov.

The number of data samples included in the dataset is 3047. 
Each data sample has 33 features.  
The label of this dataset is TARGET_deathRate.  

## Problem Statement -

This dataset is being used to predict cancer mortality rate from various
features such as average deaths per year, age, ethnicity, education level, income level,
marital status, birth rate etc.

## Models -

Linear Regression  
DNN-16  
DNN-30-8  
DNN-30-16-8  
DNN-30-16-8-4  

## Dataset Preporcessing -

Since around 75% of the data in PctSomeCol18_24 column are missing, I have
dropped this column.  
To handle the missing data of PctEmployed16_Over and PctPrivateCoverageAlone
columns, I have used median imputation where I calculated the median of all the rows
for the particular column and replaced the null value rows with the calculated median
value.  
The dataset has two columns Geography and BinnedInc the values for which are objects.
Since each row has a unique value for the Geography column, encoding methods would
not have worked so I decided to drop this column.  
For the BinnedInc column as the data is binned I had to convert it into numeric values. I
used Midpoint Transformation where I extracted the upper and lower bounds from the
ranges and calculated the midpoints.  

## Training and Test Split -

Training - 80%, Validation - 10%, Testing - 10% 

## Best Models -

Highest Performed DNN Model - DNN-30-16-8-4 Model with Adam Optimizer and LR of
0.001.  
Highest Performed Linear Regression model - Linear Regression model with Adam
Optimizer and LR of 0.1.  
