# 1- What ’re the methods that you used ?

<ul>
  <li> Functions from the <b>Data Cleaning</b> </li>
  <ul>
    <li>nfl_data.isnull().sum()</li>
    <li>missing_values_count[0:10]</li>
    <li>np.product(nfl_data.shape)</li>
    <li>missing_values_count.sum()</li>
    <li>nfl_data.dropna()</li>
    <li>nfl_data.dropna(axis=1)</li>
    <li>subset_nfl_data.fillna(0)</li>
    <li>np.random.exponential(size=1000)</li>
    <li>plt.subplots(1,2)</li>
    <li>np.random.seed(0)np.random.seed(0)</li>
    <li>np.random.seed(0)</li>
    <li>pd.to_datetime(landslides['date'], format="%m/%d/%y")</li>
    <li>before.encode("utf-8", errors="replace")</li>
    <li>after.decode("utf-8")</li>
    <li>chardet.detect(rawdata.read(10000))</li>
    <li>pd.read_csv("../input/kickstarter-projects/ks-projects-201612.csv", encoding='Windows-1252')</li>
    <li>professors['Country'] = professors['Country'].str.lower()</li>
    <li>professors['Country'] = professors['Country'].str.strip()</li>
    <li>fuzzywuzzy.process.extract("south korea", countries, limit=10, scorer=fuzzywuzzy.fuzz.token_sort_ratio)</li>
    <li>df[column].isin(close_matches)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|            <b>Function</b>                |                                       <b>Discription</b>                                |
|-------------------------------------------|-----------------------------------------------------------------------------------------|
|nfl_data.isnull().sum()|the number of missing data points per column|
|missing_values_count[0:10]|the # of missing points in the first ten columns|
|np.product(nfl_data.shape)|The Number of total missing values|
|missing_values_count.sum()|The Number of total missing values|
|nfl_data.dropna()|remove all the rows that contain a missing value|
|nfl_data.dropna(axis=1)|remove all columns with at least one missing value|
|subset_nfl_data.fillna(0)|replace all NA's with 0|
|subset_nfl_data.fillna(method='bfill', axis=0).fillna(0)|replace all the remaining na's with 0|
|np.random.exponential(size=1000)|generate 1000 data points randomly drawn from an exponential distribution|
|minmax_scaling(original_data, columns=[0])|mix-max scale the data between 0 and 1|
|fig, ax = plt.subplots(1,2)|plot both together to compare|
|np.random.seed(0)|the generator creates a random number based on the seed value|
|pd.to_datetime(landslides['date'], format="%m/%d/%y")|create a new column, date_parsed, with the parsed dates|
|before.encode("utf-8", errors="replace")|encode it to a different encoding, replacing characters that raise errors, type will be byte in stead of string|
|after.decode("utf-8")|convert it back to utf-8|
|with open("../input/kickstarter-projects/ks-projects-201801.csv", 'rb') as rawdata:result = chardet.detect(rawdata.read(10000))|look at the first ten thousand bytes to guess the character encoding|
|police_killings.to_csv("my_file.csv")|Save a version of the police killings dataset to CSV with UTF-8 encoding.|
|professors['Country'] = professors['Country'].str.lower()|convert to lower case|
|professors['Country'] = professors['Country'].str.strip()|remove trailing white spaces|
|fuzzywuzzy.process.extract("south korea", countries, limit=10, scorer=fuzzywuzzy.fuzz.token_sort_ratio)| get the top 10 closest matches to our input string|
|df[column].isin(close_matches)|get the rows of all the close matches in our dataframe|



# 3- What’s new for you ?
> <ul>
> <li>nfl_data.isnull().sum()</li>
> <li>missing_values_count[0:10]</li>
> <li>np.product(nfl_data.shape)</li>
> <li>missing_values_count.sum()</li>
> <li>nfl_data.dropna()</li>
> <li>nfl_data.dropna(axis=1)</li>
> <li>subset_nfl_data.fillna(0)</li>
> <li>np.random.exponential(size=1000)</li>
> <li>plt.subplots(1,2)</li>
> <li>np.random.seed(0)np.random.seed(0)</li>
> <li>np.random.seed(0)</li>
> <li>pd.to_datetime(landslides['date'], format="%m/%d/%y")</li>
> <li>before.encode("utf-8", errors="replace")</li>
> <li>after.decode("utf-8")</li>
> <li>chardet.detect(rawdata.read(10000))</li>
> <li>pd.read_csv("../input/kickstarter-projects/ks-projects-201612.csv", encoding='Windows-1252')</li>
> <li>professors['Country'] = professors['Country'].str.lower()</li>
> <li>professors['Country'] = professors['Country'].str.strip()</li>
> <li>fuzzywuzzy.process.extract("south korea", countries, limit=10, scorer=fuzzywuzzy.fuzz.token_sort_ratio)</li>
> <li>df[column].isin(close_matches)</li>
> </ul>

# 4- Resources ? 

> [https://www.w3resource.com/] 
> [https://docs.python.org/2/library/re.html]
> [https://pandas.org/doc/stable/] 
> [https://www.datacamp.com/]
> [http://rasbt.github.io/mlxtend/user_guide/preprocessing/minmax_scaling/]
