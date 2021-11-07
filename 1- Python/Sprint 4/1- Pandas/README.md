# 1- What ’re the methods that you used ?

<ul>
  <li> Functions from the <b>Pandas</b> </li>
  <ul>
    <li>pd.DataFrame()</li>
    <li>Series()</li>
    <li>pd.read_csv(path of the file location)</li>
    <li>pd.head()</li>
    <li>df['the data of the column']</li>
    <li>df['the data of the column'].iloc[row][column]</li>
    <li>df['the data of the column'].loc[row][column]</li>
    <li>df.describe()</li>
    <li>df.mean()</li>
    <li>df.unique()</li>
    <li>df.counts()</li>
    <li>map()</li>  
    <li>df.apply(remean_points, axis='columns')</li>  
    <li>df.groupby()</li>   
    <li>agg()</li>
    <li>sort_index()</li>  
    <li>sort_values(by=[])</li>  
    <li>reset_index()</li>   
    <li>df.dtype</li>  
    <li>df.points.astype('float64')</li>  
    <li>pd.isnull()</li>    
    <li>pd.notnull()</li>
    <li>fillna()</li>
    <li>df.replace()</li>
    <li>reviews.rename(columns={'points': 'score'}</li>
    <li>set_index()</li>
    <li>rename_axis()</li> 
    <li>concat()</li> 
    <li>. join()</li> 
    </ul>
  </ul>

# 2- Explain each method ..

|            <b>Function</b>                |                                       <b>Discription</b>                                |
|-------------------------------------------|-----------------------------------------------------------------------------------------|
|pd.DataFrame(nisted list, index= [index], columns=[columns]) | used to access a single value for a row/column label pair or to use throug it functions to sort,delete,columns|
|pd.Series([list],index=[index], name= name of list)|Series is a one-dimensional labeled array capable of holding data of any type (integer, string, float, python objects, etc.). The axis labels are collectively called index.| 
|pd.read_csv()|import and read CSV file|
|pd.head()|retrieve the first 5 rows of the data set|
|df['the data of the column']|retrieve the data of the selected column|
|df['the data of the column'].iloc[row][column]|retrieve the element from data through the index|
|df['the data of the column'].loc[row][column]|retrieve the element from data through the name of the row and column|
|df.describe()| a high-level summary of the attributes of the given column. It is type-aware|
|df.mean()|return the mean of the data|
|df.unique()|return the column data with out repeat|
|df.counts()|count the number of events for each data in column|
|map()|function executes a specified function for each item in a iterable. The item is sent to the function as a parameter.|
|df.apply(remean_points, axis='columns')|is the equivalent method if we want to transform a whole DataFrame by calling a custom method on each row|
|df.groupby()|created a group of dataset which allotted the same column values.|
|agg()|run a bunch of different functions on your DataFrame simultaneously|
|sort_index()|sort the column values|
|sort_values(by=[])|You use this to sort the Pandas DataFrame by one or more columns.|
|sort_index()|You use this to sort the Pandas DataFrame by the row index.|
|reset_index()|reset the index by creating another column for the index|
|df.dtype|the dtypes property returns the dtype of every column in the DataFrame|
|df.points.astype('float64')|convert the data type of the data to another data type|
|pd.isnull()|return true if the rows under the column have data|
|pd.notnull()|return true if the rows under the column do not have data|
|fillna()|write data instead of the none|
|df.replace()|replace in the all row undercolumn another value|
|reviews.rename(columns or index={'points': 'score'})|rename the points column with score|
|set_index()|rename index of the data frame|
|rename_axis("wines", axis='rows')|rename the axis whether the row or column|
|concat()|concatinate two data sets or more|
|left.join(right, lsuffix='_CAN', rsuffix='_UK)|combine different DataFrame objects which have an index in common|
# 3- What’s new for you ?
> <ul>
> <li>pd.DataFrame()</li>
> <li>Series()</li>
> <li>pd.read_csv(path of the file location)</li>
> <li>pd.head()</li>
> <li>df['the data of the column']</li>
> <li>df['the data of the column'].iloc[row][column]</li>
> <li>df['the data of the column'].loc[row][column]</li>
> <li>df.describe()</li>
> <li>df.mean()</li>
> <li>df.unique()</li>
> <li>df.counts()</li>
> <li>map()</li>  
> <li>df.apply(remean_points, axis='columns')</li>  
> <li>df.groupby()</li>   
> <li>agg()</li>
> <li>sort_index()</li>  
> <li>sort_values(by=[])</li>  
> <li>reset_index()</li>   
> <li>df.dtype</li>  
> <li>df.points.astype('float64')</li>  
> <li>pd.isnull()</li>    
> <li>pd.notnull()</li>
> <li>fillna()</li>
> <li>df.replace()</li>
> <li>reviews.rename(columns={'points': 'score'}</li>
> <li>set_index()</li>
> <li>rename_axis()</li> 
> <li>concat()</li> 
> <li>. join()</li>  
> </ul>

# 4- Resources ? 

> [https://www.w3resource.com/] 
> [https://docs.python.org/2/library/re.html]
> [https://pandas.org/doc/stable/] 
> [https://www.datacamp.com/]
