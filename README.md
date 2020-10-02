# House-price-predictions

House price prediction is a regression task where we have 81 features. Out of 81, 43 columns are object data type and 38 are numeric. 
In this dataset we have more object type columns than numeric.Dataset contains null or missing values also, 4 columns has more than 1100  missing values and its not worthy to 
fill these values,So i drop these columns in a dataset. After that  check the correlation between SalesPrice and other columns, drop those columns who have negative correlation.
Now fill null values with the "mean method" in numeric features and "more occurrence" method in string features. After that check unique values in categorical columns, there 
are more than 5 unique values in each categorical feature. And its time consuming task to convert each feature in numeric. Check that there is any null values in dataset. 
If not then convert the complete dataset into numeric. using 
                                                
                                                data_conv=pd.get_dummies(data,drop_first=True)


This will give converted data and I copy this in another dataframe. Now we have a total 239 features.
We need to check that which feature is important and in sklearn there is a ensemble library and pre-define model ExtraTreeRegressor, in this model predefined function is 
feature_importances_, it will give you the value of each feature.
Plot these features values on a barplot and it gives you the top 10 important features names and values.
Select these features and split the dataset  in     X_train,X_test,Y_train,Y_test.



Now check the assumptions of linear regression   5 assumptions
                                                 
                                                 1. Linear relationship
                                                 2.Assumption Normally distribution
                                                 3.assumption independent values are not correlated
                                                 4.Residual Mean
                                                 5.Homoscedasticity

After  the result of  assumptions, the conclusion is that linear regression gives an efficient value score. 
Now these assumptions show that outliers are available in a dataset, and linear regression is not applicable on outliers data. Need to remove the outliers, Z-score value helps to deduct the outliers. Z score should be less than 3, z score gives each column's values. 
Deduct the outliers dataset from the complete dataset , and split this dataset into train and test split. 
Apply linear regression, and it gives 86 score 

