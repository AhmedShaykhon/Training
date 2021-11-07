# 1- What ’re the methods that you used ?

<ul>
  <li> Functions from the <b>Pandas</b> </li>
  <ul>
    <li>spotify_data.head()</li>
    <li>spotify_data.tail()</li>
    <li>plt.figure(figsize=(16,6))</li>
    <li>sns.lineplot(data=fifa_data)</li>
    <li>plt.figure(figsize=(14,6))</li>
    <li>plt.title("Title")</li>
    <li>sns.lineplot(data=spotify_data)</li>
    <li>plt.xlabel("Date")</li>
    <li>sns.barplot(x=flight_data.index, y=flight_data['NK']</li>
    <li>sns.heatmap(data=flight_data, annot=True)</li>
    <li>sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges']</li>
    <li>sns.regplot(x=insurance_data['bmi']</li>
    <li>sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges'], hue=insurance_data['smoker'])</li>
    <li>sns.lmplot(x="bmi", y="charges", hue="smoker", data=insurance_data)</li>
    <li>sns.swarmplot(x=insurance_data['smoker'],y=insurance_data['charges'])</li>
    <li>sns.distplot(a=iris_data['Petal Length (cm)'], kde=False)</li>
    <li>sns.kdeplot(data=iris_data['Petal Length (cm)'], shade=True)</li>
    <li>sns.jointplot(x=iris_data['Petal Length (cm)'], y=iris_data['Sepal Width (cm)'], kind="kde")</li>
    <li>sns.distplot(a=iris_set_data['Petal Length (cm)</li>
    <li>plt.legend()|plt.legend()</li>
    <li>sns.set_style("dark")</li>
    <li>sns.countplot(x=my_data['SEX'])</li>
    </ul>
  </ul>

# 2- Explain each method ..

|            <b>Function</b>                |                                       <b>Discription</b>                                |
|-------------------------------------------|-----------------------------------------------------------------------------------------|
|spotify_data.head()|Print the first 5 rows of the data|
|spotify_data.tail()|Print the last five rows of the data|
|sns.lineplot(data=spotify_data)| tells the notebook that we want to create a line chart|
|plt.figure(figsize=(14,6))|set the size of the figure|
|plt.title("Title")|add title|
|sns.lineplot(data=spotify_data)|diplay the line chart of data input|
|plt.xlabel("Date")|add label date|
|sns.barplot(x=flight_data.index, y=flight_data['NK'])|tells the notebook that we want to create a par chart|
|sns.heatmap(data=flight_data, annot=True)|tells the notebook that we want to create a heat map|
|sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges'])|tells the notebook that we want to create scatter plot|
|sns.regplot(x=insurance_data['bmi'], y=insurance_data['charges'])|the line that best fits the data|
|sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges'], hue=insurance_data['smoker'])|we can color-code the points by 'smoker'|
|sns.lmplot(x="bmi", y="charges", hue="smoker", data=insurance_data)|you draw two fit lines(This command is useful for drawing multiple regression lines)|
|sns.swarmplot(x=insurance_data['smoker'],y=insurance_data['charges'])|adapt the design of the scatter plot to feature a categorical variable
(Categorical scatter plots show the relationship between a continuous variable and a categorical variable.)|
|sns.distplot(a=iris_data['Petal Length (cm)'], kde=False)| Histograms show the distribution of a single numerical variable. , kde = false means that not a smoothed histogram|
|sns.kdeplot(data=iris_data['Petal Length (cm)'], shade=True)|show an estimated, smooth distribution of a single numerical variable (or two numerical variables). , shade = True that means colored under curve|
|sns.jointplot(x=iris_data['Petal Length (cm)'], y=iris_data['Sepal Width (cm)'], kind="kde")|the curve at the top of the figure is a KDE plot for the data on the x-axis (in this case, iris_data['Petal Length (cm)']), the curve on the right of the figure is a KDE plot for the data on the y-axis (in this case, iris_data['Sepal Width (cm)'])|
|sns.distplot(a=iris_set_data['Petal Length (cm)'], label="Iris-setosa", kde=False)|create a histogram with labels|
|plt.legend()|plt.legend(): Force legend to appear (for any plot type)|
|sns.set_style("dark")|Change the style of the figure to the "dark" theme|
|sns.countplot(x=my_data['SEX'])|Create a bar figure to observe the counts of male and female|


# 3- What’s new for you ?
> <ul>
> <li>spotify_data.head()</li>
> <li>spotify_data.tail()</li>
> <li>plt.figure(figsize=(16,6))</li>
> <li>plt.title("Title")</li>
> <li>sns.lineplot(data=spotify_data)</li>
> <li>plt.xlabel("Date")</li>
> <li>sns.barplot(x=flight_data.index, y=flight_data['NK']</li>
> <li>sns.heatmap(data=flight_data, annot=True)</li>
> <li>sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges']</li>
> <li>sns.regplot(x=insurance_data['bmi']</li>
> <li>sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges'], hue=insurance_data['smoker'])</li>
> <li>sns.lmplot(x="bmi", y="charges", hue="smoker", data=insurance_data)</li>
> <li>sns.swarmplot(x=insurance_data['smoker'],y=insurance_data['charges'])</li>
> <li>sns.distplot(a=iris_data['Petal Length (cm)'], kde=False)</li>
> <li>sns.kdeplot(data=iris_data['Petal Length (cm)'], shade=True)</li>
> <li>sns.jointplot(x=iris_data['Petal Length (cm)'], y=iris_data['Sepal Width (cm)'], kind="kde")</li>
> <li>sns.distplot(a=iris_set_data['Petal Length (cm)</li>
> <li>plt.legend()|plt.legend()</li>
> <li>sns.set_style("dark")</li>
> <li>sns.countplot(x=my_data['SEX'])</li>
> </ul>

# 4- Resources ? 

> [https://www.w3resource.com/] 
> [https://docs.python.org/2/library/re.html]
> [https://pandas.org/doc/stable/] 
> [https://www.datacamp.com/]
