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
> Based on Domain Knowledge, removing the type of house which doesn't match with sqft value. For example, consider 1bhk there should be min of 300sqft. So removing the records where there is a value less than 300sqft. similarly we apply this for all types of houses.
  
> Removing the outliers of feature "Price" using normal distribution.(taking mean and std and considering only values greater than mean-std and less than mean+std).

> Also there is price flaw for 2bhk and 3bhk. In general, the price of 3bhk should be higher than 2bhk. But there are few records of price for 3bhk less than 2bhk. This can be viewed with a scatter plot of specific location and taking the parameters as total sqft and price.

> The logic used to remove these outliers is that taking the mean of all 2bhk price values and checking whether the 3bhk price is less or greater to that. If we got any value lesser than mean of 2bhk, then we create separate list and drop these values in the main DataFrame.

> Removing outliers in "bhk" and "bath" features. There are values where more number of bathrooms than bhk which is unreal. So I kept a parameter stating that count of bath should be < bhk +2. If it exceeds then I removed these outliers.

*Changing categorical to numerical*
> Using get_dummies method I have changed the "location" feature categorical values to numerical. This method will convert the categories into numerical by creating separate columns.

> Now I have the final DataFrame with all numerical values and now this is ready for the next step.

*Model Building and Predictions*
> X and y values are splitted using the final dataframe. where X has all features except the target price feature and y has only price feature.

> As the target price feature is numerical data. I took the basic Linear Regression model and fitted the X_train and y_train values to it. and checked the score using testing data. It really performed well.

> Also used GridSearchCV in order to consider multiple algorithms and also tuned the parameters in each.and got the scores for each algorithm with best parameters for that algorithm. Even Here LinearRegression performed better.

> Now that I saved this LR model using pickle and also X.columns which have all column features using json.

*Building Website and Server*

> As in our approach, the user gives gata of sqft and other parameters like numer of bhk,number of bath,location.

> To get the user input I build a simple website using html css and javascript which helps to connect to the server.

> This data is uploaded to the server and server is connected to the backend where our saved models are present which will return price of the house.

> server.py has the code for server which connects the util.py (where the saved models are present) and app.html and app.cs (this has code for website).And app.js will post the user input to the server.py and and gets the price results from server.py









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
