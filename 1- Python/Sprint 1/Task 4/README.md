## 1- What ’re the methods that you used ?
> There are many important methods used and the target of these methods is to focus on the pandas library and the functions which support this library such as pd.read_csv(csv_path), dataframe.head(), dataframe.shape, dataframe.dtypes, dataframe.info(), dataframe.rename(columns={'x':'length','y':'width','z':'depth'}, inplace=True), dataframe.loc[(df_diamonds['cut']=='Good')|(df_diamonds['cut']=='Very Good'), ['cut']], dataframe.mean(axis=1), dataframe['cut'].count, df_diamonds.isnull().sum(). these powerfull functions is helpful to deal with datasets.


## 2- Explain each method ..
> ### Every function has its signature to handle the input and output parameters. So we will talk about every function related to our target.
> 1. firstly you have to use the pd.read_csv(csv_path) for reading the data set from local or link of the uploaded file.
> 2. df_diamonds.head() this function is used to knew the first 5 elements of the data set. to give you a hint about the columns and the first 5 rows of the data.
> 3. df_diamonds.shape this is the object of data frame class which has the size of the data frame (number of the rows and columns).
> 4. df_diamonds.dtypes this is the object of data frame class which has the data types of the data wich inserted in our data set.
> 5. df_diamonds.info() this is function return data summary (data type, columns' names).
> 6. df_diamonds.loc[(df_diamonds['x']>5)| (df_diamonds['y']>5)|(df_diamonds['z']>5), ['x','y','z']] this is function which return columns depend on its condition.
> 7. df_diamonds.rename(columns={'x':'length','y':'width','z':'depth'}, inplace=True) this function target to rename the header of the columns.
> 8. df_diamonds.describe() this is function to describe the data set in details.
> 9. df_diamonds.mean(axis=1) this is function to get the mean of the columns
> 10. df_diamonds[['price']].mean(axis=1) this is function return the mean of 'price' column only
> 11. df_diamonds[['price']].mean(axis=0) this is function calculate the mean of price for each cut of diamonds DataFrame.
> 12. df_diamonds[['price']].describe() this is function calculates count, minimum, maximum price for each cut of diamonds DataFrame.
> 13. df_diamonds[['price']].describe() this is function counts how many times each value in cut series of diamonds DataFrame occurs. value_counts().
> 14. df_diamonds.isnull().sum() this is function counts the number of missing values in each Series of diamonds DataFrame.

## 3- What’s new for you ?
> Practice in writing and searching for the functions and remind all useful libraries and functions is very important for the next steps.

## 4- Resources ? 
> [https://www.w3resource.com/] [https://www.w3schools.com/python/python_lists.asp] [https://www.coursera.org/learn/python-for-applied-data-science-ai?specialization=applied-artifical-intelligence-ibm-watson-ai]
