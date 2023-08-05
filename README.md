# House Price Prediction using ML

## Exploratory Data Analysis on various Datasets

## Table of Contents

1. Problem Statement
2. Dataset along with features .
3. Approach Used to solve the Problem
4. Explanation along with the Code 
5. Results with Screenshots

**1. PROBLEM STATEMENT**: 
> A retail company "ABC Private Limited" wants to understand the customer purchase behaviour (specifically, purchase amount)
against various products of different categories.They have shared purchase summary of various customers for selected high volume products from last month, The dataset also contains customer demographics (age, gender, marital status, city_type, stay_in_current_city), product details (produck_ id and product category) and Total purchase_amount from last month. Now, they want to build a model which it is done after the cleaning in order to predict the purchase amount of customer against products which will help them to create personalized offer for customers against different products.

**2. DATASET**: 
> https://www.kaggle.com/datasets/sdolezel/black-friday?select=test.csv (Downloaded the zip file which has both train and test data files separately)

> Features: UserID, Product_ID, Gender Age, Occupation, City_Category, Stay_In_Current_City_Years, Marital_Status, Product_Category_1, Product_Category_2,    Product_Category_3, Purchase

**3. APPROACH USED to solve the Problem**: 

* *As our problem statement shows that we have to do the data cleaning and feature engineering for this dataset.The following steps are done to achieve this.* 

> Cleaning of data is done by dropping unnecessary columns

> Changing categorical values of columns to numericals using various techniques

> Filling the missing values of each columns using different methods

> Visualising the cleaned data to extract insights/Observations

> Finalled scaled the cleaned data as training and test in order to build the model for prediction








**4. Explanation along with the Code**:

> Importing the necessary libraries to perform dataset operations which are numpy,pandas,matplotlib,seaborn

> Reading the data of both train.csv and test.csv files using PANDAS READ method

> checking the general information of data by using methods called INFO(),DESCRIBE()

> Dropping the unnecessary column by DROP method

> Changing categorical values of each column to numerical by MAPping function

> Filling the missing values by using MODE statistical operation(which is efficient one !)

> Changing all column datatypes to int using ASTYPE() method

> Visualising the cleaned data by using seaborn library and plotting the graphs (i.e BARPLOT) and extracting the insight (as in our dataset
  it shows PRODUCT_CATEGORY1 has high number of purchases. This can be seen by using graphs)
  
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
