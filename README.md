# House-price-predictions
House price prediction is a regression task where we have 81 features. Out of 81, 43 columns are object datatye and 38 are numeric. 
In this dataset we have more object type columns than numeric.Dataset contains null or missing values also, 4 columns has more than 1100  missing values and its not worthy to fill
these values,So i drop these columns in a dataset. After that  check the correlation between SalesPrice and other columns, drop those columns who have negative correlation.
Now fill null values with the "mean method" in numeric features and "more occurency" method in string features. After that check unique values in categorical columns, there are more than 5 unique values in each categorical feature. And its time consuming task to convert each feature in numeric. Check that there is any null values in dataset. If no then convert complete dataset into numeric. using           data_conv=pd.get_dummies(data,drop_first=True)
This will gives converted data and i copy this in other dataframe. Now we have total 239 features.
We need to check that which feature is important and in sklerarn there is a ensemble library and pre-define model ExtraTreeRegressor, in this model pre-define function is 
feature_importances_, it will gives you the value of each feature.
Plot these features values on barplot and it gives you the top 10 important features name and values.
Select these features and split dataset in     X_train,X_test,Y_train,Y_test.
Now check the assumptions of linear regression  5 assumptions
                                                 1. Linear relationship
                                                 2.Assumption Normally distribution
                                                 3.assumption independent values are not correlated
                                                 4.Residual Mean
                                                 5.Homoscedasticity

After  the result of  assumptions, conclusion is linear regression is gives efficient value score. 
Now these assumptions shows that outliers are available in dataset, and linear regression is not applicable on outliers data. Need to remove the outliers, Z-score value help to deduct the outliers. Z score should be less than 3, z score gives the each columns values. 
Deduct the outliers dataset from complete dataset , and split this dataset into train and test split. 
Apply linear regression, and it gives 86 score 
