# House Price Prediction using ML

## End to End ML Project

## Table of Contents

1. Problem Statement
2. Dataset along with features .
3. Approach Used to solve the Problem
4. Explanation along with the Code 
5. Results with Screenshots

**1. PROBLEM STATEMENT**: 
> As city is growing larger,There's need for predicting the prices of different types of houses in order for a people to take the lease. So it is needed to predict the price based on considerable features.This can be acheived by ML model. 

**2. DATASET**: 
> https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data 

> Features: area_type,availability,location,size,society,total_sqft,bath,balcony,price

**3. APPROACH USED to solve the Problem**: 

* *As our problem statement shows that we have to build a model that predicts the house price. The following steps are done to achieve this.* 

> Cleaning of data is done by dropping unnecessary columns

> Changing categorical values of columns to numericals using various techniques

> In location feature changing the categorical values which are repeated less to "Other".

> Removing the outliers in bhk and bath features.

> Built LR model to predict the house price.








**4. Explanation along with the Code**:

*Data import and cleaning(by dropping features and null values)*
> Importing the necessary libraries to perform dataset operations which are pandas,matplotlib,seaborn

> Reading the data using PANDAS READ method.

> Dropping the unnecessary columns("availability","area_type","society","balcony") by DROP method.

> Checked the null value counts and dropped these because they are less in number.

*Feature Engineering*
> Changed categorical "size" feature to numerical by split method.

> In feature "total_sqft" we separate values which are in range (for example: 2100-2500) with normal floating values.

> Taking average in "total_sqft" feature where the feature values which are in certain range.

> Grouping the feature "location" with freq. count of each value in location feature in order to reduce the dimensionality of this feature.

> Changing the feature "location" values of count less than 10 to "Other"

*Detecting the Outliers & Removing it*
> Based on Domain Knowledge, removing the type of house 
  
> Scaling the features into train and test. Approach used here is that the rows(null values of target column)  are splitted into test data.

> Now it is ready to train the model after using TRAIN_TEST_SPLIT function from sklearn










**5. Results with Screenshots**: 

> 1. Reading data

<img width="750" alt="Screenshot 2023-04-27 at 2 04 42 PM" src="https://user-images.githubusercontent.com/88378136/234806998-1fa8031a-4609-4972-9444-6fcfbf01fe15.png">

> 2. Changing categorical values to numerical

<img width="750" alt="Screenshot 2023-04-27 at 2 04 59 PM" src="https://user-images.githubusercontent.com/88378136/234807868-0b9abf87-10be-43f4-8c90-aeb4ec06dedb.png">

> 3. Filling the missing values

<img width="750" alt="Screenshot 2023-04-27 at 2 05 11 PM" src="https://user-images.githubusercontent.com/88378136/234808025-0c42e356-a47f-4306-b6d8-3f5ba35af585.png">

> 4. Visualising the graphs of cleaned data to extract insight

<img width="750" alt="Screenshot 2023-04-27 at 2 05 26 PM" src="https://user-images.githubusercontent.com/88378136/234808180-87388a88-acd7-49e7-b683-bdb2970cd157.png">

> 5. Finally!!! Feature scaling is done! (Now the data is ready to perform in training of the model)

<img width="750" alt="Screenshot 2023-04-27 at 2 05 41 PM" src="https://user-images.githubusercontent.com/88378136/234808228-eefaf084-9cb9-4759-a702-36a6a11fe9fa.png">


# Fake_Review
